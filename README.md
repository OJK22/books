# Library Book Management UI

A React + TypeScript single-page application for the book-catalog and circulation-management interface of a library system.

> This repository contains the frontend application. Its API is served separately.

## Features represented in the current source

- Dashboard
- Book catalog browsing and updates
- Add-book workflow
- Barcode book workflow
- Book deletion workflow
- Reports
- Login screen and protected application routes

The application uses API endpoints through the Vite development proxy. Real data access and authorization depend on the backend service.

## Technology

- React 18 and TypeScript
- Vite
- React Router
- Tailwind CSS and shadcn/ui
- TanStack Query
- Vitest and ESLint

## Requirements

- Node.js and npm compatible with the versions declared in `package.json` and `package-lock.json`.

## Run locally

```bash
npm ci
npm run dev
```

The Vite development server is configured to use port `5001`.

## Quality checks

```bash
npm run lint
npm test
npm run build
```

These are the scripts declared by the project; run them locally or in CI before treating a change as verified.

## API configuration and security notes

The development proxy targets are defined in `vite.config.ts`. They currently point to HTTP hosts. Production deployments must use HTTPS and a secure server-side proxy/API configuration.

The current route guard includes a no-token preview exception for localhost and hostnames containing `lovable.app`. Keep preview behavior out of production builds. Frontend route guards are only a user-interface convenience; the backend must enforce authentication and authorization for every data operation.

## Related repositories

- [Main library frontend](https://github.com/OJK22/front)
- [Staff administration UI](https://github.com/OJK22/admin)
- [Lending prototype](https://github.com/OJK22/loan)

## License and project rights

No open-source license is currently included. Do not assume permission to reuse or redistribute this code until the rights holder(s) have selected and added an OSI-approved license. Confirm any municipal and team ownership obligations first.
