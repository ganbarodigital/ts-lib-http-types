# CHANGELOG

## Introduction

This CHANGELOG tells you:

* when a release was made
* what is in each release

It also tells you what changes have been completed, and will be included in the next tagged release.

For each release, changes are grouped under these headings:

* _Backwards-Compatibility Breaks_: a list of any backwards-compatibility breaks
* _New_: a list of new features. If the feature came from a contributor via a PR, make sure you link to the PR and give them a mention here.
* _Fixes_: a list of bugs that have been fixed. If there's an issue for the bug, make sure you link to the GitHub issue here.
* _Dependencies_: a list of dependencies that have been added / updated / removed.
* _Tools_: a list of bundled tools that have been added / updated / removed.

## develop branch

The following changes have been completed, and will be included in the next tagged release.

## v0.1.4

Released Thursday, 20th February 2020.

### Refactor

* Now republishes internal types from `@ganbarodigital/ts-lib-error-reporting`
  - this was done to address problems with circular dependencies

## v0.1.3

### Fixes

* Introduced `internal.ts` to resolve circular dependencies within the package.

### Dependencies

* Remove dependenciy on `@ganbarodigital/ts-lib-packagename` (causes circular dependency hell)

## v0.1.2

Released Thursday, 20th February 2020.

### Dependencies

* Added `@ganbarodigital/ts-lib-packagename`

## v0.1.1

Released Thursday, 20th February 2020.

### Dependencies

* Updated to the latest release of `@ganbarodigital/ts-lib-error-reporting`

## v0.1.0

Released Thursday, 20th February 2020.

### Backwards-Compatibility Breaks

* Updated error callbacks to use `@ganbarodigital/ts-lib-error-reporting`

## v0.0.2

Released Wednesday, 19th February 2020.

### Dependencies

* Do not depend on an unreleased version of ValueObjects!

## v0.0.1

Released Wednesday, 19th February 2020.

### New

* Added `HttpStatusCode` type
* Added `httpStatusCodeFrom()` smart constructor
* Added `isHttpStatusCode()` data guard
* Added `mustBeHttpStatusCode()` data guarantee
