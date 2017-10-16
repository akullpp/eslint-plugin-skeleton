# eslint-plugin-skeleton

## Deprecation Warning

It is recommended that you use Vue, React or even Angular 2 at this point.

## Description

ESLint Plugin with recommended rules and mixins for the different environments of an Angular web application.

## Integration

Either insert it as a local folder with a relative path in the `package.json` (see [akSkeleton](https://github.com/akullpp/akSkeleton)) or use it as node module.

Your root `.eslintrc` needs to look the following:

```json
{
  "extends": "./node_modules/eslint-plugin-skeleton/config/eslintrc.base"
}
```

The `.eslintrc` located in your source files (e.g. `src/`) should extend the browser mixin:

```json
{
  "extends": "../node_modules/eslint-plugin-skeleton/config/mixins/browser"
}
```

The `.eslintrc` located in your test files (e.g. `test/`) should extend the test mixin:

```json
{
  "extends": "../node_modules/eslint-plugin-skeleton/config/mixins/test"
}
```

## Configuration & Mixins

1. The `eslintrc.base` contains all the defaults and main rules. It ensures that the root files are linted as a node environment.
2. The `browser` mixin sets up the rules and environment for linting client-side scripts.
3. The `test` mixin is exclusively used for the test environment.
