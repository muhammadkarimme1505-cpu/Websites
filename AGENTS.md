# Development Instructions

These permanent instructions apply throughout this repository and to future full-stack web applications developed here.

## Default Technologies

- Frontend: Next.js, React, TypeScript, and Tailwind CSS.
- Backend: Node.js, NestJS, and TypeScript.
- Database: PostgreSQL with Prisma.
- Containers: Docker.

These technologies are defaults. Change them when project requirements justify it, and document the chosen stack and rationale in README.md.

## Architecture and Code Quality

- Use clean, modular architecture with clear boundaries and focused modules.
- Keep frontend and backend responsibilities separate. Keep database access, secrets, and privileged business logic on the server.
- Write secure, maintainable TypeScript with strict typing and explicit interfaces at module boundaries.
- Follow existing project conventions and avoid unnecessary complexity.

## Security and Configuration

- Validate all incoming data at trust boundaries, including API requests, route parameters, query strings, and external service responses.
- Implement secure authentication and enforce authorization on the server for every protected operation.
- Use established authentication libraries, secure password hashing when passwords are used, and appropriate session or token protections.
- Never hardcode passwords, API keys, tokens, or other secrets. Use environment variables and never commit secret values.
- Validate required environment configuration at startup and avoid exposing secrets in client bundles, logs, or errors.

## Database and APIs

- Use database migrations for schema changes. Review migrations and preserve existing data; do not perform destructive database operations without explicit permission.
- Use Prisma for database access by default and keep database concerns within the backend.
- Document backend APIs with Swagger/OpenAPI, including request validation, responses, and authentication requirements.

## Testing and Documentation

- Write meaningful unit and integration tests for business logic, API behavior, database interactions, authentication, and authorization.
- Run relevant tests and checks for changes, and report failures or checks that could not be run accurately.
- Maintain README.md with architecture, prerequisites, setup, development, testing, migration, and Docker instructions as applicable.
- Maintain .env.example with required variable names and safe placeholder values, never real credentials.

## User Changes and Git

- Inspect existing files and changes before editing. Never overwrite, discard, or revert existing user changes.
- If a requested change conflicts with user changes, preserve them and ask for clarification.
- Never create commits or push without the user's explicit permission.
