# Client-Side Development Guide

Welcome to the `client` directory! This folder contains the front-end application, built with [Vite](https://vitejs.dev/), using React and TypeScript.

## Prerequisites

- **Node.js** v20 or above
- **npm** (comes with Node.js)
- [Optional] Docker, if you want to build/run the client in a container

---

## Local Development

To start developing the client locally:

1. **Install dependencies**  
   Run this command in the `client` directory to install project packages:
   ```bash
   npm install
   ```

2. **Start the development server**  
   This spins up Vite's dev server with hot-reload on [http://localhost:3000](http://localhost:3000):
   ```bash
   npm run dev
   ```

3. **Lint and format your code**  
   (If configured) Use the following commands to check code style and types:
   ```bash
   npm run lint
   npm run typecheck
   ```

---

## Build for Production

To generate a production-ready static build:

```bash
npm run build
```

The built files will be output to the `dist/` directory.

---

## Running with Docker

For consistent builds and deployments, a `Dockerfile` is provided. The container will:

- Install dependencies
- Build the app
- Serve static files on port 3000

To build and run:

```bash
docker build -t my-client-app .
docker run -p 3000:3000 my-client-app
```

---

## Additional Notes

- The app is configured to use module aliases via `tsconfig.json` (`@/*` for local imports).
- If you change dependencies or configuration, remember to rebuild the Docker image.
- Static files served from `dist/` in production via the `serve` package.

---

For questions on client architecture or environment setup, check with the project maintainers.
