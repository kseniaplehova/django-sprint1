# Blogicum — Sprint 1: pages and templates

A Django blog skeleton: URL routing, function-based views and a template hierarchy, with posts served from an in-memory list.

Educational project — Yandex Practicum, Python Developer course. This is **stage 1 of 3** of the Blogicum project (see also `django-sprint3` and `django-sprint4`).

## Features

- Two Django apps: `blog` (posts) and `pages` (static pages "About" and "Rules").
- Function-based views: post list (newest first), post detail by `id` (404 for unknown posts) and a category page.
- URL routing with namespaces and path converters (`<int:id>`, `<slug:category_slug>`).
- Template inheritance: `base.html` plus reusable `header` and `footer` includes.
- Posts are stored in a Python list in `blog/views.py`; there are no models or database tables yet (introduced in sprint 3).

## Tech stack

Python, Django 5.1.1, pytest, pytest-django, flake8 (see `requirements.txt`).

## Getting started

```bash
git clone https://github.com/kseniaplehova/django-sprint1.git
cd django-sprint1
python -m venv venv
source venv/Scripts/activate   # Windows (Git Bash); on Linux/macOS: source venv/bin/activate
pip install -r requirements.txt
cd blogicum
python manage.py runserver
```

Open http://127.0.0.1:8000/.

## Tests

Run from the repository root:

```bash
pytest
```

The suite in `tests/` checks project structure, settings, URLs, views, templates and HTML output.

## Author

Ksenia Plehova — [GitHub](https://github.com/kseniaplehova)
