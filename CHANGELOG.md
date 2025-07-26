# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2024-01-XX

### Added
- Initial release of Django Audit Library
- Automatic model change tracking (CREATE, UPDATE, DELETE)
- User authentication tracking (login, logout, failed attempts)
- Data export auditing
- System event logging
- Security monitoring middleware
- Comprehensive Django admin interface
- Thread-safe request context handling
- Migration-safe operation detection
- Utility functions for manual logging
- Performance monitoring for slow requests
- Geographic tracking for login attempts
- Configurable audit settings

### Features
- **AuditLog Model**: Tracks all model changes with before/after values
- **LoginAttempt Model**: Monitors authentication attempts and failures
- **DataExport Model**: Audits data exports with metadata
- **SystemEvent Model**: Captures system errors and events
- **AuditMiddleware**: Core request tracking functionality
- **SecurityAuditMiddleware**: Additional security monitoring
- **Admin Interface**: Read-only views with advanced filtering
- **Utility Functions**: Manual logging helpers
- **Thread-Local Storage**: Request context preservation
- **Migration Detection**: Automatic skip during migrations

### Security
- Tracks suspicious request patterns
- Monitors unusual user agents
- Logs security-related events
- IP address and session tracking
- Geographic location support

### Performance
- Efficient database queries with proper indexing
- Minimal performance impact
- Configurable to skip certain models/actions
- Automatic detection of slow requests

### Compatibility
- Django 3.2+
- Python 3.8+
- Thread-safe operation
- Migration-safe deployment