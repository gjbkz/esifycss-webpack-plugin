# esifycss-webpack-plugin

> **Development has moved to the [esifycss monorepo](https://github.com/gjbkz/esifycss).**
>
> This package is now maintained in [`packages/esifycss-webpack-plugin`](https://github.com/gjbkz/esifycss/tree/main/packages/esifycss-webpack-plugin).
> The npm package name remains `esifycss-webpack-plugin`. Use the [current documentation](https://github.com/gjbkz/esifycss/tree/main/packages/esifycss-webpack-plugin#readme), and report issues or submit pull requests in [gjbkz/esifycss](https://github.com/gjbkz/esifycss).
>
> The maintained 0.2.x release line requires **Node.js 22 or newer** and **Webpack 5**.
> The documentation below describes the legacy standalone release.

[![Test](https://github.com/kei-ito/esifycss-webpack-plugin/actions/workflows/test.yml/badge.svg)](https://github.com/kei-ito/esifycss-webpack-plugin/actions/workflows/test.yml)
[![codecov](https://codecov.io/gh/kei-ito/esifycss-webpack-plugin/branch/master/graph/badge.svg)](https://codecov.io/gh/kei-ito/esifycss-webpack-plugin)

This plugin adds a resolver for [EsifyCSS](https://github.com/kei-ito/esifycss).
The resolver resolves `*.module.css` to `*.modules.css.js` or `*.modules.css.ts`.

## Usage

Add this plugin to your `webpack.config.js`.

```javascript
const EsifyCSSWebpackPlugin = require('esifycss-webpack-plugin');

module.exports = {
  ...{}, // other configurations
  plugins: [
    new EsifyCSSWebpackPlugin(),
  ],
};
```

## Development

Use Node.js 26 for dependency installation, builds, lint, and tests (`npm ci`, `npm run lint`, `npm test`). CI also runs the compiled package and resolver tests on Node.js 12, 14, 16, 22, and 24 to verify runtime compatibility.
