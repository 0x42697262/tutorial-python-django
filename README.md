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

## Handling Errors

Handling database errors can be handled by adding an HTTP 404 response.

```python
from django.http import Http404

try:
    question = Question.objects.get(pk=question_id)
except Question.DoesNotExist:
    raise Http404("Question does not exist")
return render(request, "polls/detail.html", {"question": question})

```

### Shortcuts
The error handling above can be shortened to using the shortcuts library.
```python
from django.shortcuts import render, get_object_or_404


question = get_object_or_404(Question, pk=question_id)
return render(request, "polls/detail.html", {"question" : question})
```
