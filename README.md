# Understanding TypeScript Training

This repo is created for own use based on [Udemy Understanding TypeScript course](https://www.udemy.com/course/understanding-typescript).

## Setting up a basic project

### Recommended extensions

* ESLint
* Material Icon Theme
* Path Intellisense
* Prettier - Code formatter

### Setup TypeScript development

* Download and Install **Node.js** - https://nodejs.org/en/download/prebuilt-installer
* Instal TypeScript `npm install -g typescript`

### Create the first TypeScript project

In the project folder:

* `npm init`
* `npm install --save-dev lite-server`
* create app.ts file
* compile app.ts => `tsc app.ts` => app.js file will be created
* edit package.json file, add to scripts:

```json
"scripts": {
    ...
    "start": "lite-server"
  },
```

To use start script: `npm run start` (or just simplay: `npm start`)

## TypeScript compiler

Generate JavaScript file from TypeScript file:

* compile a single \*.ts: `tsc app.ts`
* to automatic recompile use watch mode: `tsc app.ts -w`

Initizite a TypeScript project: `tsc --init`

* the init command will generate a TypeScript project config file: `tsconfig.json`
* to compile all \*.ts file in TypeScipt project: `tsc`
* watch mode: `tsc *.ts -w`

### TypeScript configuration - tsconfig.json

* exclude files: `"exclude" : [ "**/*.dev.ts", "analytics.dev.ts" ]`
  * "node_modules" is excluded by default
* include files `"include" : [ "app.ts" ]`
  * additional included files
  * \*\*/\*.ts files are included by default

#### Compiler options (`"compilerOptions": { ... } `)

* **target**: JavaScript version to compile
  * ES5 (default) is an older version (ECMAScript 5 - 2009), but it is compatible with IE
  * ES6 is newer JavaScript version (ECMAScript 2015), all modern browser support it (not compatible with IE)
  * for more info about [JavaScript Versions](https://www.w3schools.com/Js/js_versions.asp)
* **module**: (later...)
* **lib**: specify libraries to be included
  * if it not specified, the compiler will include all library related to target JavaScript version
  * e.g.: `"dom"`: acces to document, console, etc.
  * default setup for ES6: `"lib": [ "dom", "es6", "dom.iterable", "scripthost" ]`


