# Node Package Starter

A minimal TypeScript starter for creating npm packages with support for CommonJS, ESM, and TypeScript definitions.

---

## Features

- ⚡ TypeScript
- 📦 Build with [tsup](https://tsup.egoist.dev)
- 📜 Outputs CJS, ESM, DTS
- ✨ ESLint + Prettier preconfigured

---

## Getting Started

### 1. Clone and Install

```bash
git clone https://github.com/egiev/node-package-starter.git <package_name>
cd <package_name>
npm install
```

### 2. Configure your package

```json
{
  "name": "@your-scope/your-package",
  "version": "0.1.0",
  "description": "Your package description",
  "author": "Your Name",
  "license": "MIT",
  "repository": {
    "type": "git",
    "url": "git+https://github.com/your-username/your-package.git"
  },
  "bugs": {
    "url": "https://github.com/your-username/your-package/issues"
  },
  "homepage": "https://github.com/your-username/your-package#readme"
}
```

### 3. Update README

Replace this README content with information about your package.

### 4. Start coding

Write your code in src/.

Example src/index.ts:

```ts
export function hello(name: string): string {
  return `Hello, ${name}! 👋`;
}
```

### 5. Build the package

```bash
npm run build
```

This generates:

- dist/index.js → CommonJS build
- dist/index.mjs → ESM build
- dist/index.d.ts → TypeScript types
- dist/index.d.mts → ESM TypeScript types

### 6. Test locally

```bash
npm pack
# produces your-package-1.0.0.tgz
npm install ../path-to/your-package-1.0.0.tgz
```

### 7. Lint & format

```bash
npm run lint
npm run lint:fix
npm run format
```

### 8. Publish

```bash
npm login
npm version patch   # or minor / major
npm publish --access public
```

## Usage

### ESM

```ts
import { hello } from '@your-scope/your-package';

console.log(hello('World'));
```

### CommonJS

```js
const { hello } = require('@your-scope/your-package');

console.log(hello('World'));
```

## License

This project is licensed under the [MIT](./license)
