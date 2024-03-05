# EsbuildScssAssetIssues

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 17.2.2.

## Expected behaviour

When building the project with the esbuild `application` builder, assets required by SCSS files using variables in the URLs are resolved.

## Actual behaviour

Assets are not found.

## Regression

This worked with the old `@angular-devkit/build-angular:browser` builder.

## Demo

```shell
## Install dependencies
npm ci

## To build with the application builder, run:
npm run build

## To build with the old browser builder, run:
npm run build-legacy
```

## Use case

We consume an SCSS library which uses variables for the paths to the assets. Switching to the esbuild `application` builder has broken the builds for our app.
