# Django Audit Library

## Installation Instructions

### For Development

1. Clone or download this library
2. Install in development mode:
```bash
pip install -e .
```

### For Production

1. Build the package:
```bash
python -m build
```

2. Install from the built package:
```bash
pip install dist/django_audit_library-1.0.0-py3-none-any.whl
```

### Publishing to PyPI

1. Install build tools:
```bash
pip install build twine
```

2. Build the package:
```bash
python -m build
```

3. Upload to PyPI:
```bash
twine upload dist/*
```

## Quick Start

1. Add to INSTALLED_APPS:
```python
INSTALLED_APPS = [
    # ... your apps
    'audit',
]
```

2. Add middleware:
```python
MIDDLEWARE = [
    # ... your middleware
    'audit.middleware.AuditMiddleware',
    'audit.middleware.SecurityAuditMiddleware',  # Optional
]
```

3. Run migrations:
```bash
python manage.py migrate audit
```

That's it! The audit system will now automatically track all model changes, user logins, and system events.