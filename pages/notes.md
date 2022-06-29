---
title: Notes - Merlin Alex
display: Notes
subtitle: Quick notes / tips
description: Quick notes / tips
---

<article>

## .eslintrc

_2022/06/09_

**Install**
```bash
pnpm add -D eslint @antfu/eslint-config
```
**Configuration**
```json
{
  "extends": "@antfu",
  "rules": {
    "no-undef": "off",
    "comma-dangle": [
      "warn",
      "never"
    ],
    "@typescript-eslint/comma-dangle": "off",
    "arrow-parens": [
      "warn",
      "as-needed"
    ],
    "no-console": "off"
  }
}
```

**package.json**

```json
{
  "scripts": {
    "lint": "eslint .",
    "lint:fix": "eslint . --fix"
  }
}
```

## .prettierrc

_2022/01/13_

```json
{
  "semi": false,
  "singleQuote": true,
  "trailingComma": "none",
  "arrowParens": "avoid"
}
```

</article>
