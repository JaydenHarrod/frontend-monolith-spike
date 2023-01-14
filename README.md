# Frontend Monolith

## CLI

- `pnpm run dev` run development environment
- `pnpm run build` build static assets
- `pnpm run lint` lint code
- `pnpm run e2e:test` run tests against preview build

## Architecture Todo

- `storybook`: previewing `ui` components
- `tRPC/Prisma/zod`: e2e data type safety
- `simple-analytics`: data tracking
- `sentry`: error tracking

## What's inside?

This Turborepo includes the following packages/apps:

### Apps and Packages

- `nextjs`: create [t3](https://nextjs.org/) app w/ Prisma, NextAuth, tRPC
- `web`: another [Next.js](https://nextjs.org/) app with [Tailwind CSS](https://tailwindcss.com/)
- `ui`: a stub React component library with [Tailwind CSS](https://tailwindcss.com/) shared by both `web` and `docs` applications
- `eslint-config-custom`: `eslint` configurations (includes `eslint-config-next` and `eslint-config-prettier`)
- `tsconfig`: `tsconfig.json`s used throughout the monorepo

Each package/app is 100% [TypeScript](https://www.typescriptlang.org/).

### Building packages/ui

This example is setup to build `packages/ui` and output the transpiled source and compiled styles to `dist/`. This was chosen to make sharing one `tailwind.config.js` as easy as possible, and to ensure only the CSS that is used by the current application and its dependencies is generated.

### Utilities

This Turborepo has some additional tools already setup for you:

- [Tailwind CSS](https://tailwindcss.com/) for styles
- [TypeScript](https://www.typescriptlang.org/) for static type checking
- [ESLint](https://eslint.org/) for code linting
- [Prettier](https://prettier.io) for code formatting
- [Remote Caching](https://turbo.build/repo/docs/core-concepts/remote-caching) for quick development
- `react-hook-form`: managing form state
- `dayjs`: handling date time
