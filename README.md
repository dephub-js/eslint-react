# @dephub/eslint-react ⚛️

> Opinionated modern ESLint configuration for React projects, built on top of `@dephub/eslint-ts`.

[![NPM version](https://img.shields.io/npm/v/@dephub/eslint-react.svg?style=flat)](https://npmjs.org/package/@dephub/eslint-react)
[![ESM-only](https://img.shields.io/badge/ESM-only-brightgreen?style=flat)](https://nodejs.org/)

---

## Features ✨

- ⚛️ Extends `@dephub/eslint-ts` for full TS + React support
- 🧠 React and React Hooks best practices
- 🟦 Strict TypeScript rules included
- 🔀 Import sorting and unused import handling
- 🧹 Prettier-compatible formatting rules

---

## Installation 📦

- npm: `npm install -D eslint @dephub/eslint-react`
- pnpm: `pnpm add -D eslint @dephub/eslint-react`
- yarn: `yarn add -D eslint @dephub/eslint-react`
- bun: `bun add -D eslint @dephub/eslint-react`

> Since this config extends `@dephub/eslint-ts`, make sure your project is configured for TypeScript.

---

## Usage 🎯

### API 🧩

Create an `eslint.config.mjs` file:

```ts id="reactcfg"
import { defineConfig } from 'eslint/config';
import reactConfig from '@dephub/eslint-react';

export default defineConfig(reactConfig);
```

You don’t need to manually include `@dephub/eslint-ts` — it’s already extended internally.

### Extending the configuration

```ts id="reactext"
import { defineConfig } from 'eslint/config';
import reactConfig from '@dephub/eslint-react';

export default defineConfig([
  ...reactConfig,
  {
    rules: {
      'react/react-in-jsx-scope': 'off',
    },
  },
]);
```

Then run ESLint normally:

```bash id="reactrun"
npx eslint .
```

---

## License 📄

MIT License – see [LICENSE](LICENSE) for details.

**Author:** Estarlin R ([estarlincito.com](https://estarlincito.com))
