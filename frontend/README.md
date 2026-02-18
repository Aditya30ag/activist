# Frontend Setup Guide

This guide will help you set up the frontend development environment for the activist platform.

## Prerequisites

- **Node.js**: Version 18 or higher
- **Yarn**: Version 4.12.0 (recommended package manager)
- **Git**: For version control

## Tech Stack

The frontend is built with:

- **Nuxt 4**: Vue.js meta-framework
- **Vue 3**: Progressive JavaScript framework
- **TypeScript**: Type-safe JavaScript
- **Tailwind CSS 4**: Utility-first CSS framework
- **Pinia**: State management
- **Vue I18n**: Internationalization
- **Playwright**: End-to-end testing
- **Vitest**: Unit testing

## Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/activist-org/activist.git
cd activist
```

### 2. Install Dependencies

```bash
cd frontend
yarn install
```

### 3. Environment Setup

Copy the environment configuration file:

```bash
cp ../.env.dev.example ../.env.dev
```

Edit the `.env.dev` file to configure your environment variables.

### 4. Start Development Server

```bash
# For local development
yarn dev:local

# Or regular development
yarn dev
```

The application will be available at `http://localhost:3000`.

## Available Scripts

### Development
- `yarn dev` - Start development server
- `yarn dev:local` - Start with local environment configuration

### Building
- `yarn build` - Build for production
- `yarn build:local` - Build with local environment
- `yarn generate` - Generate static site
- `yarn preview` - Preview production build

### Testing
- `yarn test` - Run unit tests
- `yarn test:local` - Run comprehensive local tests
- `yarn test:comprehensive` - Run all tests including e2e
- `yarn test:auth` - Run tests with authentication
- `yarn test:clean` - Clean and run tests

### Code Quality
- `yarn typecheck` - Run TypeScript type checking
- `yarn lint` - Run ESLint
- `yarn format` - Check code formatting with Prettier

### Maintenance
- `yarn restart:types` - Clean and reinstall dependencies

## Environment Variables

Key environment variables for the frontend:

- `VITE_BACKEND_URL` - Backend API URL (default: `http://localhost:8000`)
- `VITE_FRONTEND_URL` - Frontend URL (default: `http://localhost:3000`)
- `VITE_BACKEND_URL_PROXY` - Backend proxy URL for production

## Development Workflow

### 1. Making Changes

- Edit files in the `app/` directory for pages and components
- Use `components/` for reusable Vue components
- Store state in `stores/` using Pinia
- Add utilities in `shared/utils/`

### 2. Testing

Always run tests before committing:

```bash
yarn typecheck
yarn lint
yarn test
```

### 3. Building

Test production build locally:

```bash
yarn build
yarn preview
```
### Getting Help

- Check the [main README](../README.md) for project overview
- Review [CONTRIBUTING.md](../CONTRIBUTING.md) for contribution guidelines
- Join our [Matrix chat](https://matrix.to/#/#activist_community:matrix.org)
- Open an issue on [GitHub](https://github.com/activist-org/activist/issues)

## Deployment

### Production Build

```bash
yarn build
```

### Docker

A Dockerfile is provided for containerized deployments:

```bash
docker build -t activist-frontend .
```

### Netlify

The frontend is configured for Netlify deployment with static generation.

## Contributing

We welcome contributions! Please read our [contributing guide](../CONTRIBUTING.md) before submitting pull requests.

### Development Guidelines

- Follow the [style guide](../STYLEGUIDE.md)
- Write tests for new features
- Ensure accessibility compliance
- Use TypeScript for type safety
- Follow Vue 3 and Nuxt 4 best practices

## License

This project is licensed under the AGPL-3.0-or-later license. See [LICENSE.txt](../LICENSE.txt) for details.
