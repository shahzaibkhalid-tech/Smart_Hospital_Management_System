# SHMS Project Rules & Guidelines

## 1. Architectural Principles
- **Modularity**: Every major feature must reside in its own NestJS module.
- **Clean Architecture**: Strictly separate concerns between Controllers (HTTP), Services (Business Logic), and Prisma (Data Access).
- **SOLID Principles**: Follow SOLID principles to ensure the codebase remains maintainable and scalable.

## 2. Coding Standards
- **Naming Conventions**:
  - Classes/Interfaces: `PascalCase` (e.g., `PatientService`)
  - Variables/Functions: `camelCase` (e.g., `getPatientById`)
  - Files: `kebab-case.extension` (e.g., `auth.controller.ts`)
- **TypeScript**: Use strict typing. Avoid `any` at all costs.
- **Linting**: All code must pass `npm run lint` before being committed.
- **Formatting**: Use Prettier for consistent code formatting.

## 3. API & Documentation
- **RESTful**: Follow REST best practices (correct status codes, HTTP methods).
- **Swagger**: Every controller method must be documented using `@ApiTags`, `@ApiOperation`, and `@ApiResponse`.
- **Versioning**: All APIs must be versioned (e.g., `/api/v1/`).
- **Validation**: Use `class-validator` and `class-transformer` in DTOs for all request payloads.

## 4. Database Management
- **Prisma**: Use Prisma for all database operations.
- **Migrations**: Never modify the database schema manually. Always use `npx prisma migrate dev`.
- **Seeding**: Maintain a seed script for development and testing data.

## 5. Security Protocols
- **Authentication**: Use JWT-based authentication.
- **Authorization**: Implement Role-Based Access Control (RBAC) using custom decorators and guards.
- **Passwords**: Never store plain-text passwords. Use `bcrypt` for hashing.
- **Sanitization**: Always validate and sanitize user input to prevent SQL injection and XSS.

## 6. Error Handling
- **Global Filter**: Use a global exception filter to ensure consistent error responses.
- **Logging**: Log all errors with sufficient context for debugging.

## 7. Testing Strategy
- **Unit Tests**: Write unit tests for all service logic using Jest.
- **E2E Tests**: Implement end-to-end tests for critical business flows.
- **Coverage**: Aim for at least 80% code coverage.
