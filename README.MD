# eslint config

## Configure

1. Configure project to read packages started from `@pswind` from github package registry by running
```bash
npm config set @pswind:registry=https://npm.pkg.github.com --userconfig ./.npmrc
```

2. Install npm package
```bash
npm install --save-dev eslint @pswind/eslint-config prettier
```
3. Create `.eslintrc.js` file with following content
```js
module.exports = {
  extends: '@pswind/eslint-config',
  parserOptions: {
    project: './tsconfig.json', // Specify path to your tsconfig file
  }
}

```
4. Create `.prettierrc.js` file locally:
```js
module.exports = {
  "printWidth": 120,
  "tabWidth": 2,
  "useTabs": false,
  "semi": true,
  "singleQuote": true,
  "trailingComma": "all",
  "bracketSpacing": true,
  "bracketSameLine": false,
  "arrowParens": "always",
  "quoteProps": "consistent",
  "endOfLine": "lf"
}