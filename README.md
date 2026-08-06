# Django Learning

Today I worked on authentication.

## 1. Out-of-the-Box User Model
Django provides a robust, built-in `User` model right from the start. It handles usernames, emails, passwords, and user flags (like `is_staff`, `is_active`, `is_superuser`) without requiring any custom database schema design.

## 2. Secure Password Hashing
Django never stores raw passwords. It uses secure-by-default PBKDF2 hashing with a SHA256 cryptographic hash. This ensures user passwords remain highly secure against database breaches, while still allowing developers to swap in stronger algorithms (like Argon2 or bcrypt) easily.

## 3. Granular Group and Permission System
Django includes an intuitive permission system that associates permissions with models. It allows assigning permissions to specific users or to user groups (e.g., editors, customers, administrators). Views can then easily enforce these permissions via helper decorators like `@permission_required` or mixins like `PermissionRequiredMixin`.
