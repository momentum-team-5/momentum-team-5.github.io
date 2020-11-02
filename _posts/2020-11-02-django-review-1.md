---
layout: post
title: Django Review - Models
tags: phase-3 django
---

Today, we will focus on understanding the database, how Django models interact with it, and how to model data for specific problems.

## Assignment

This week, you will work on [Habit Tracker](https://classroom.github.com/a/47PanCbE). For Wednesday, you will want to have all your models created.

## Data modeling problems for small groups

Small groups (use Google Meet or Zoom):

- Charlette, Nathan, Jon, Phil
- Kim, Derek, Babacar, Tom

**Problem 1:** You want to make an application for yourself to hold your favorite recipes. This application does not have users; since it's just for you, there is no log in or registration. Recipes have ingredients and recipe steps. They also have "tags," which allow you to put arbitrary categories on them like "breakfast", "kid-friendly", or "vegetarian." Each recipe can have multiple tags; each tag can have multiple recipes. What's the data model?

**Problem 2:** Take the above problem. You now want to make it so other people can use your application. Each person has their own recipes they own. Recipes can be public or private; private ones are only visible to the user who made it. What's the new data model?

**Problem 3:** Take a simple version of Twitter. Users can make posts. Each post can have many images. Users can follow other users in order to see a list of posts from everyone they follow. Users can "like" posts to designate that they think it's a great post. What's the data model?

**Problem 4:** Take the above problem. You want to make it more like Facebook. Users don't have a one-way follow; instead, they have "friends," which is a two-way relationship. In addition, users can comment on their friends' posts. What's the data model?

**Problem 5:** Imagine a system for a library. The library has one or more copies of each book it owns. Users can check out individual copies of a book and the library needs to know who currently has the book. Books are due two weeks after check out. First, what questions do you need to ask to complete this data model? For these questions, decide on an answer. Then, what's the data model?

## Resources

- [Data modeling explained in 10 minutes](https://www.credera.com/insights/data-modeling-explained-in-10-minutes-or-less/)
- [Logical database design using entity-relationship modeling](https://www.ibm.com/support/knowledgecenter/SSEPEK_11.0.0/intro/src/tpc/db2z_logicaldbdesignentityrelationshp.html) - This looks intimidating and is part of a manual for a database we won't use, but is _really good material_.
- [Django model relationships](https://docs.djangoproject.com/en/3.0/topics/db/models/#relationships)
- [Django model queries](https://docs.djangoproject.com/en/3.0/topics/db/queries/)
- [Video: Building effective Django queries with expressions](https://www.youtube.com/watch?v=a-sfr6y_hY8&list=PL2NFhrDSOxgXXUMIGOs8lNe2B-f4pXOX-&index=9) - DjangoCon 2019 video on queries
