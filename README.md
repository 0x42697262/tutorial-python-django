# What is this about?
Just me trying to log stuffs about my progress in learning [Django](https://www.djangoproject.com).

Each tutorials from the [Django Documentation](https://docs.djangoproject.com/en/4.2/intro/tutorial01/) are separated into multiple branches named by its tutorial number.

# Usage

Install the required packages `pip install -r requirements.txt` and start the server `python managed.py runserver`.


# Tutorial

[Tutorial 3](https://docs.djangoproject.com/en/4.2/intro/tutorial03/)

## Writing views and using templates.

Using `render()` replaces the need to import `loader` and `HttpResponse`. Importing `render()` shortcut can be done through
```python
from django.shortcuts import render
```
