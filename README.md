# Rules

Rules I use in my AI Agents.

## Prompt

Coding guidelines

```md
## Coding Guidelines

### TypeScript/JavaScript

- Never use any; Almost never use "as"
- Aim for end-to-end type safety
- Let the compiler infer response types whenever possible
- Always use named exports; Don't use default exports unless you have to
- Don't have an index file only for exports
- Prefer async/await over Promise().then()
- Unused vars should start with _ (or never exist at all)
- Prefer string literals over string concatenation
- Don't abbreviate; use descriptive names
- Always use early return over if-else
- Prefer hash-lists over switch-case
- Follow programming language naming conventions (SCREAMING_SNAKE_CASE for constants, camelCase for functions, kebab-case for file names)
- Use strict null checks and avoid optional chaining for critical paths
- Prefer readonly interfaces for function parameters
- Use type predicates for runtime type validation
- Avoid type assertions - use type guards or proper typing instead
- Prefer interface over type for object definitions
- Use const assertions for literal values
- Prefer template literals over string concatenation
- Use object destructuring for function parameters
- Prefer functional programming patterns over imperative
- Use async/await error handling with try/catch
- Validate external data with Zod or similar libraries
- Use descriptive error messages with context
- Prefer composition over inheritance
- Write pure functions without side effects
- Use immutable data structures when possible
- Prefer map/filter/reduce over for loops
- Use optional parameters instead of method overloading
- Prefer readonly arrays for immutable data
- Use brand types for nominal typing
- Prefer conditional types over overloads
- Use satisfies operator for explicit type checking
- Prefer type inference for simple cases
- Use namespace imports for large modules (import * as)
- Prefer descriptive boolean variable names (isVisible over flag)
- Use early returns to reduce nesting
- Prefer descriptive variable names over comments
- Write self-documenting code with clear intent

## Coding guidelines for automated tests

- Write tests for business logic, not implementation
- Prefer integration tests over unit tests
- Use test databases for database operations
- Mock external dependencies appropriately
- Use descriptive test names (should...when...)
- Prefer async/await in tests over callbacks
- Use snapshot testing sparingly
- Test error cases and edge conditions
- Use coverage thresholds as safety net
- Prefer real browser testing over mocks
- Write tests before fixing bugs
- Use realistic test data
- Test accessibility requirements
- Use visual regression testing for UI components

## Node.js / Backend development

- Use async/await for all I/O operations
- Implement proper error handling middleware
- Use structured logging with correlation IDs
- Prefer async middleware for Express apps
- Use environment variables for configuration
- Implement health check endpoints
- Use connection pooling for database connections
- Prefer async file operations
- Use process managers for production (PM2)
- Implement proper shutdown handlers
- Use request validation middleware
- Prefer functional middleware composition
- Use compression for response bodies
- Implement rate limiting for public APIs
- Use HTTPS and security headers
- Validate all user input
- Use environment-based configuration
- Implement proper CORS policies
- Use helmet.js for security headers
- Prefer async/await over callbacks
- Use proper status codes in responses
- Implement request timeouts
- Use structured error responses
- Document APIs with OpenAPI/Swagger

### Project Structure

- Use monorepo for related packages
- Prefer feature-based organization over type-based
- Prefer explicit imports over barrel files
- Use clear separation between shared and feature-specific code

### Coding Guidelines for React

- Don't declare constants or functions inside components; keep them pure
- Don't fetch data in useEffect, use React Query/TanStack Query
- Don't use magic strings for cache tags; use an enum/factory
- Don't use magic numbers/strings
- Use enum for react query cache strings
- Prefer Suspense and useSuspenseQuery over react query isLoading
- Use errorBoundary with retry button
- Use TypeScript for all new components
- Prefer functional components with hooks
- Use custom hooks for reusable logic
- Keep components small and single-responsibility
- Use proper typing for props with interfaces
- Prefer composition over prop drilling
- Use Context API for global state sparingly
- Memoize expensive computations with useMemo
- Use useCallback for stable function references
- Prefer controlled components over uncontrolled
- Use error boundaries for graceful error handling
- Implement proper loading states
- Use React.memo for expensive re-renders
- Prefer CSS-in-JS with TypeScript support
- Use testing-library for component testing
- Write integration tests over unit tests
- Use React DevTools for performance profiling
- Use fragment shorthand <> when possible
- Avoid inline arrow functions in JSX props
- Destructure props at the component definition
- Implement proper keyboard navigation and a11y
- Use meaningful component and prop names

#### If using using Next.js

- Prefer server components for data fetching
- Use Next.js App Router for new projects

### Security

- Validate all user input
- Use parameterized queries to prevent SQL injection
- Sanitize user-generated content

## Git Workflow

- Use conventional commits (feat, fix, docs, style, refactor, test, chore)
- Keep commits small and focused - one logical change per commit
- Write descriptive commit messages in imperative mood
- Rebase instead of merge when updating feature branches
- Squash merge PRs to maintain clean history
- Protect main branch - require PR reviews and status checks
- Use semantic versioning for releases
- Create feature branches from main
- Delete ***merged*** branches regularly
- Use .gitignore appropriately for your stack
- Sign commits when required by project
```

Prevent gambiarra

- from [taelin](https://x.com/VictorTaelin/status/1974115859473019256)

```md
## NO GAMBIARRA POLICY - ASK FOR FEEDBACK INSTEAD

Due to the difficulty of implementing this codebase, we must strive to keep the
code high quality, clean, modular, simple and functional - more like an Agda
codebase, less like a C codebase. Gambiarras, hacks and duct taping must be
COMPLETELY AVOIDED, in favor of robust, simple and general solutions.

In some cases, you will be asked to perform a seemingly impossible task, either →
because it is (and the user is unaware), or because you don't grasp how to do it
properly. In these cases, DO NOT ATTEMPT TO IMPLEMENT A HALF-BAKED SOLUTION JUST
TO SATISFY THE USER'S REQUEST. If the task seems too hard, be honest that you
couldn't solve it in the proper way, leave the code unchanged, explain the
situation to the user and ask for further feedback and clarifications.
The user is a domain expert that will be able to assist you in these cases.
```
