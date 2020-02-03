# Basic Types for the HTTP Protocol

## Introduction

This TypeScript library provides some basic types to describe the HTTP protocol. Use it to improve the type-safety of your code.

## Quick Start

```
# run this from your Terminal
npm install @ganbarodigital/ts-lib-http-types
```

```typescript
// add this import to your Typescript code
import { HttpStatusCode } from "@ganbarodigital/ts-lib-http-types/lib/v1"
```

__VS Code users:__ once you've added a single import anywhere in your project, you'll then be able to auto-import anything else that this library exports.

## V1 API

### HttpStatusCode

```typescript
/**
 * represents any HTTP status code in the range `100` to `599` inclusive
 */
export type HttpStatusCode = Branded<number, "@ganbarodigital/HttpStatusCode">;
```

`HttpStatusCode` is a _type_. At runtime, it resolves down to a native Javascript `number`.

## NPM Scripts

### npm run clean

Use `npm run clean` to delete all of the compiled code.

### npm run build

Use `npm run build` to compile the Typescript into plain Javascript. The compiled code is placed into the `lib/` folder.

`npm run build` does not compile the unit test code.

### npm run test

Use `npm run test` to compile and run the unit tests. The compiled code is placed into the `lib/` folder.

### npm run cover

Use `npm run cover` to compile the unit tests, run them, and see code coverage metrics.

Metrics are written to the terminal, and are also published as HTML into the `coverage/` folder.