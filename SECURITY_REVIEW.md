# Security review notes

## Findings requiring follow-up
- `ProtectedRoute` allows access without a token on `localhost` and any hostname containing `lovable.app`. Confirm this is strictly a preview-only build path; it must never be enabled in a production deployment.
- The login flow stores the bearer token in local storage. Any script executing in the application origin can read it; use a server-managed HttpOnly cookie if the API supports that session model.
- Client-side route protection is not authorization. The API must enforce authentication and authorization for every operation, including create, update, delete, and report endpoints.

## Changes in this branch
- Ignore local `.env*` files while allowing a committed `.env.example` template.
- No tracked files were deleted.
