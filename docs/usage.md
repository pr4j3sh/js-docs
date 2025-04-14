---
title: Usage
id: usage
slug: /usage
---

# Usage

- Create `jsdoc.json` file in your project's root directory

```json
{
  "tags": {
    "allowUnknownTags": true,
    "dictionaries": ["jsdoc", "closure"]
  },
  "source": {
    "include": ["src"],
    "includePattern": ".+\\.(j|t)s(doc|x)?$",
    "excludePattern": "(^|\\/|\\\\)_"
  }
}
```

- Create `config.json` file in your project's root directory

```json
{
  "locales": ["ko"],
  "outDir": "./docs/docs/api",
  "localesDir": "./docs/i18n/{locale}/docusaurus-plugin-content-docs/current/api",
  "sidebar": "./docs",
  "prefix": "api/",
  "jsdoc": "./jsdoc.json"
}
```

- Install `jsdoc-to-mdx` as a dev dependency

```bash
npm i -D jsdoc-to-mdx
```

- Add this line to your `package.json` in scripts

```json
{
  "scripts": {
    "docs": "npx jsdoc-to-mdx -c config.json"
  }
}
```

- Create docs scaffold

```bash
npm run docs
```

- View docs

```bash
cd docs
npm run start
```

> View docs in your browser.
