---
layout: post
title: 'Setting Up Python'
tags: phase-2 python python3 pipenv exercism
---

Great work this morning, y'all. Here's everything you need to do to set up Python for this phase.

### Install exercism
Open a terminal and enter the following command verbatim (the && chains commands together, but only if the first one doesn't fail):
	
	
	brew update && brew install exercism
	

Exercism is a great tool we'll be using for doing warmup and learning exercises.

### Install pipenv
Open a terminal and enter the following command verbatim:
	
	
	brew install pipenv
	

pipenv is a package management tool that will simplify the task of organizing complex Python projects.

### Get to know Python
I'm including a few links to good beginner resources for anyone who's eager to get started.
	
- [Real Python Python Basics](https://realpython.com/python-basics/)
	
- [Official Python Beginner's Resources](https://wiki.python.org/moin/BeginnersGuide/NonProgrammers)
	
- [Official Python Tutorial](https://docs.python.org/3/tutorial/index.html)
	
- [Python Library & Language Documentation (bookmark this site)](https://docs.python.org/3/index.html)


### Quick note on Python 2 vs Python 3
There are two major versions of Python in common use -- Python 2 and Python 3. Python 2 is no longer updated and support is being withdrawn, but because MacOS uses Python 2 in a few places, Python 2 is the default version. This is annoying and complicates things somewhat, but isn't too difficult to navigate around -- if you're trying out code you found on the internet, and it says (for example):
	
	python a_python_script.py
	

you should instead run:

	
	python3 a_python_script.py
	

There are a couple of other places where you may need to run slightly different commands, but I'll only go over one of them right now; if you try some of the exercism.io exercises this weekend,
it may tell you to run:

	
	pytest hello_world_test.py
	

Instead, you should run:

	
	python3 -m pytest hello_world_test.py
	

(of course, hello_world_test.py could be any Python file).
