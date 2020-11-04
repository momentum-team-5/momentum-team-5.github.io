---
title: "Django Review Day 2: Models and Views"
tags: phase-3 django
layout: post
---

Today we talked about creating models and building views. We specifically went over the 5 big views used everywhere in Django.

## The Five Views

```py
# - list many models
def cohort_list(request):
    cohorts = Cohort.objects.all()
    return render(request, "core/cohort_list.html", {"cohorts": cohorts})


# - show one model
def cohort_detail(request, pk):
    cohort = get_object_or_404(Cohort, pk=pk)
    return render(request, "core/cohort_detail.html", {"cohort": cohort})


# - create a model
def cohort_create(request):
    if request.method == "GET":
        form = CohortForm()
    else:
        form = CohortForm(data=request.POST)
        if form.is_valid():
            cohort = form.save()
            return redirect("cohort-detail", pk=cohort.pk)

    return render(request, "core/cohort_create.html", {"form": form})


# - update a model
def cohort_update(request, pk):
    cohort = get_object_or_404(Cohort, pk=pk)

    if request.method == "GET":
        form = CohortForm(instance=cohort)
    else:
        form = CohortForm(instance=cohort, data=request.POST)
        if form.is_valid():
            cohort = form.save()
            return redirect("cohort-detail", pk=cohort.pk)

    return render(request, "core/cohort_update.html", {"cohort": cohort, "form": form})


# - delete a model
def cohort_delete(request, pk):
    cohort = get_object_or_404(Cohort, pk=pk)

    if request.method == "POST":
        cohort.delete()
        return redirect("cohort-list")

    return render(request, "core/cohort_delete.html", {"cohort": cohort})
```

## Other Resources

- [The sample app from class](https://github.com/momentum-team-5/example--project-board)
- [URLs Lead the Way](https://www.mattlayman.com/understand-django/urls-lead-way/) and [Views on Views](https://www.mattlayman.com/understand-django/views-on-views/) from Understand Django
