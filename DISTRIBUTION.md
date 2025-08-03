# Distribution Guide for Django Audit Library

## Quick Distribution Methods

### 1. GitHub Repository (Recommended)
1. Create a new repository on GitHub
2. Upload all files from `django_audit_library/` folder
3. Create a release with the wheel file attached
4. Users can install with:
   ```bash
   pip install https://github.com/mcwamsie/django_audit_library.git
   ```

### 2. PyPI (Python Package Index)
1. Install publishing tools:
   ```bash
   pip install twine
   ```
2. Upload to PyPI:
   ```bash
   twine upload dist/*
   ```
3. Users install with:
   ```bash
   pip install django-audit-library
   ```

### 3. Direct File Distribution
- Share the `.whl` file from `dist/` folder
- Users install with:
  ```bash
  pip install django_audit_library-1.0.0-py3-none-any.whl
  ```

### 4. Private Package Repository
- Use tools like:
  - **DevPI**: Private PyPI server
  - **Artifactory**: Enterprise repository
  - **Nexus**: Repository manager
  - **AWS CodeArtifact**: Cloud-based artifact repository

## File Locations
- **Wheel file**: `dist/django_audit_library-1.0.0-py3-none-any.whl`
- **Source**: `dist/django_audit_library-1.0.0.tar.gz`
- **Complete package**: Entire `django-audit-library/` folder

## Installation Instructions for Users
Include these instructions with your distribution:

```bash
# Method 1: From wheel file
pip install path/to/django_audit_library-1.0.0-py3-none-any.whl

# Method 2: From GitHub (if uploaded)
pip install git+https://github.com/mcwamsie/django_audit_library.git

# Method 3: From PyPI (if published)
pip install django-audit-library

# Method 4: Development installation
pip install -e path/to/django-audit-library/
```