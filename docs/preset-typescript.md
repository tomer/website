---
id: babel-preset-typescript
title: babel-preset-typescript
sidebar_label: typescript
---

This preset includes the following plugins:

- [@babel/plugin-transform-typescript](https://github.com/babel/babel/tree/master/packages/babel-plugin-transform-typescript)

> You will need to specify `--extensions ".ts"` for `@babel/cli` & `@babel/node` cli's to handle `.ts` files.

## Example

**In**

```javascript
const x: number = 0;
```

**Out**

```javascript
const x = 0;
```

## Installation

```sh
npm install --save-dev @babel/preset-typescript
```

## Usage

### Via `.babelrc` (Recommended)

**.babelrc**

```json
{
  "presets": ["@babel/preset-typescript"]
}
```

### Via CLI

```sh
babel --presets @babel/preset-typescript script.ts
```

### Via Node API

```javascript
require("@babel/core").transform("code", {
  presets: ["@babel/preset-typescript"]
});
```

## Options

### `jsxPragma`

`string`

Replace the function used when compiling JSX expressions.

This is so that we know that the import is not a type import, and should not be removed

