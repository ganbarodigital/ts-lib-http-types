# Basic Types for the HTTP Protocol

![Node.js CI](https://github.com/ganbarodigital/ts-lib-http-types/workflows/Node.js%20CI/badge.svg)

## Introduction

This TypeScript library provides some basic types to describe the HTTP protocol. Use it to improve the type-safety of your code.

- [Introduction](#introduction)
- [Quick Start](#quick-start)
- [V1 API](#v1-api)
  - [HttpStatusCode](#httpstatuscode)
  - [httpStatusCodeFrom()](#httpstatuscodefrom)
  - [isHttpStatusCode()](#ishttpstatuscode)
  - [mustBeHttpStatusCode()](#mustbehttpstatuscode)
- [NPM Scripts](#npm-scripts)
  - [npm run clean](#npm-run-clean)
  - [npm run build](#npm-run-build)
  - [npm run test](#npm-run-test)
  - [npm run cover](#npm-run-cover)

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

### httpStatusCodeFrom()

```typescript
export function httpStatusCodeFrom(input: number, onError?: OnError): HttpStatusCode;
```

`httpStatusCodeFrom()` is a _smart constructor_. It converts input `numbers` into `HttpStatusCode` types at compile time.

### isHttpStatusCode()

```typescript
/**
 * data guard. checks to see if the `input` value is in the range
 * of HTTP status codes.
 *
 * returns `true` if `input` is a number between 100 and 599 inclusive.
 */
export function isHttpStatusCode(input: number): boolean;
```

`isHttpStatusCode()` is a _data guard_. Use it to check that a given number is a valid HTTP status code.

### mustBeHttpStatusCode()

```typescript
/**
 * data guarantee. calls the supplied `onError()` handler if the `input`
 * number is not a valid HTTP status code.
 */
export function mustBeHttpStatusCode(input: number, onError: OnError): void
```

`mustBeHttpStatusCode()` is a _data guarantee_. Use it to make sure that a given number is a valid HTTP status code.

## Internal Note

This package simply republishes internal types from [@ganbarodigital/ts-lib-error-reporting](https://github.com/ganbarodigital/ts-lib-error-reporting/).

The types used to live in here. Unfortunately, we ran into a lot of trouble with circular dependencies (which broke unit testing).

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