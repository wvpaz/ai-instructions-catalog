# Front-end Template Model: React / Next.js

This document outlines the template model for setting up a front-end application using Next.js, React, and TypeScript.

## Technologies & Dependencies

*   **Framework**: Next.js (`latest`)
*   **Language**: TypeScript (`^5.0.0`)
*   **UI Library**: React (`latest`), React DOM (`latest`)
*   **Runtime**: Node.js (compatible with Next.js)
*   **Package Manager**: npm (or yarn/pnpm compatible with `package.json`)
*   **Testing**: Vitest (`^1.4.0`) with `@testing-library/react`, `@testing-library/jest-dom`, `jsdom`, `@vitejs/plugin-react`
*   **Linting**: ESLint (`^8.0.0`) with `eslint-config-next`, `@typescript-eslint/eslint-plugin`, `eslint-config-prettier`, `eslint-plugin-prettier`
*   **Formatting**: Prettier (`^3.0.0`)

## Key Configuration Files

*   `package.json`: Contains project metadata, scripts (dev, build, start, lint, format, test), and dependencies.
    *   **Scripts**: `dev`, `build`, `start`, `lint`, `format`, `test`
    *   **Main Dependencies**: `next`, `react`, `react-dom`
    *   **Dev Dependencies**: `typescript`, `eslint`, `eslint-config-next`, `prettier`, `@types/node`, `@types/react`, `@types/react-dom`, `@testing-library/jest-dom`, `@testing-library/react`, `vitest`, `jsdom`, `@vitejs/plugin-react`, `@typescript-eslint/eslint-plugin`, `@typescript-eslint/parser`
*   `next.config.mjs`:
    *   Basic Next.js configuration.
*   `tsconfig.json`:
    *   **Target**: `es2015`
    *   **Module**: `esnext`
    *   **Module Resolution**: `bundler`
    *   **JSX**: `react-jsx`
    *   **Strict Checks**: `strict`
    *   **Other**: `allowJs`, `esModuleInterop`, `incremental`, `isolatedModules`, `noEmit`, `resolveJsonModule`, `skipLibCheck`
    *   **Paths**: `@/*`: `./*`
    *   **Plugins**: `next`

## Project Structure (Core)

```
<project-root>/
├── app/
│   ├── layout.tsx
│   ├── page.tsx
│   └── page.test.tsx
├── public/
├── next-env.d.ts
├── next.config.mjs
├── package.json
├── tsconfig.json
├── vitest.config.ts
├── vitest.setup.ts
├── .eslintrc.json
├── .prettierignore
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
    npm run dev
    ```
4.  **Environment Variables**: Create `.env.local` based on `.env.example` (if provided), configuring necessary environment variables such as API endpoints for connecting to back-end services.

## Development Workflow

*   **Front-end Development**: Develop Next.js pages, layouts, and React components.
*   **Testing**: Run tests with `npm run test` or in watch mode with `npm run test:watch`.
*   **Code Standards**: Run `npm run lint` and `npm run format`.
*   **API Integration**: Consume REST API endpoints provided by back-end services.

