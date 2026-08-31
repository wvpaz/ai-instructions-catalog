# Back-end Template Model: NestJS

This document outlines the template model for setting up a back-end service using Node.js, NestJS, and TypeScript.

## Technologies & Dependencies

*   **Framework**: NestJS (`^10.0.0`)
*   **Language**: TypeScript (`^5.1.3`)
*   **Runtime**: Node.js (compatible with NestJS 10)
*   **Package Manager**: npm (or yarn/pnpm compatible with `package.json`)
*   **Testing**: Vitest (`^1.4.0`) with `@nestjs/testing`, `ts-jest`
*   **Linting**: ESLint (`^8.42.0`) with `@typescript-eslint/eslint-plugin`, `eslint-config-prettier`, `eslint-plugin-prettier`
*   **Formatting**: Prettier (`^3.0.0`)

## Key Configuration Files

*   `package.json`: Contains project metadata, scripts (start, build, test, lint, format), and dependencies.
    *   **Scripts**: `start:dev`, `start:prod`, `build`, `test`, `lint`, `format`
    *   **Main Dependencies**: `@nestjs/common`, `@nestjs/core`, `@nestjs/platform-express`, `reflect-metadata`, `rxjs`
    *   **Dev Dependencies**: `@nestjs/cli`, `@nestjs/schematics`, `@nestjs/testing`, `typescript`, `vitest`, `ts-jest`, `eslint`, `prettier`
*   `nest-cli.json`:
    *   `collection`: `@nestjs/schematics`
    *   `sourceRoot`: `src`
    *   `compilerOptions.deleteOutDir`: `true`
*   `tsconfig.json`:
    *   **Target**: `ES2021`
    *   **Module**: `commonjs`
    *   **OutDir**: `./dist`
    *   **Strict Checks**: `strictNullChecks`, `noImplicitAny`, `strictBindCallApply`
    *   **Decorators**: `emitDecoratorMetadata`, `experimentalDecorators`
    *   **Other**: `declaration`, `removeComments`, `sourceMap`, `incremental`, `skipLibCheck`, `forceConsistentCasingInFileNames`, `allowSyntheticDefaultImports`, `resolveJsonModule`

## Project Structure (Core)

```
<project-root>/
├── src/
│   ├── main.ts
│   ├── app.module.ts
│   ├── app.controller.ts
│   ├── app.service.ts
│   └── ... (other modules, controllers, services)
├── test/
│   ├── app.controller.spec.ts
│   └── ... (other test files)
├── package.json
├── nest-cli.json
├── tsconfig.json
├── tsconfig.build.json
├── vitest.config.ts
├── vitest.setup.ts
├── .eslintrc.js
├── .gitignore
└── .prettierrc
```

## Initial Setup Steps

1.  **Clone Repository / Navigate to Directory**:
    ```bash
    git clone <repository-url>
    cd <project-directory>
    ```
2.  **Install Dependencies**:
    ```bash
    npm install
    ```
3.  **Run Development Server**:
    ```bash
    npm run start:dev
    ```
4.  **Database Setup**: (Specifics depend on chosen database and ORM/ODM. E.g., for PostgreSQL/MySQL and Drizzle/TypeORM, configure database connection and run migrations/seeders.)
5.  **Environment Variables**: Create `.env` file based on `.env.example` (if provided), configuring necessary API keys, database connections, ports, JWT secrets, etc.

## Development Workflow

*   **Back-end Development**: Develop NestJS modules, controllers, and services following modular architecture.
*   **Testing**: Run tests with `npm run test` or in watch mode with `npm run test:watch`.
*   **Code Standards**: Run `npm run lint` and `npm run format`.
*   **API Exposure**: Expose REST endpoints to be consumed by client applications / front-ends.

