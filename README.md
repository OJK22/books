# Library Book Management UI

A React + TypeScript single-page application for book-catalog and circulation-management workflows.

## Features

The current interface includes book catalog browsing and maintenance, add-book and barcode workflows, reports, and protected application routes. Actual data access and authorization are provided by a separately hosted API.

## Technology

- React 18 and TypeScript
- Vite and React Router
- Tailwind CSS and shadcn/ui
- TanStack Query
- Vitest and ESLint

## Requirements

Use a supported Node.js version and npm.

## Run locally

```bash
npm ci
npm run dev
```

## Quality checks

```bash
npm run lint
npm test
npm run build
```

Run these checks before submitting changes. The presence of a script does not imply that it currently passes in every environment.

## Security

The frontend is not an authorization boundary. The backend must validate identity and permissions for every operation. Use HTTPS in production, keep secrets out of browser bundles, and never commit real credentials or personal data.

## Related projects

- [Main library frontend](https://github.com/OJK22/front)
- [Staff administration UI](https://github.com/OJK22/admin)
- [Lending prototype](https://github.com/OJK22/loan)

## Contributing

Please open an issue before large changes. Pull requests should be focused, explain the motivation, include test coverage where practical, and report the checks you ran.

## License

MIT. See [LICENSE](./LICENSE).
