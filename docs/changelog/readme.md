---
lang: en-US
title: Changelog | Guzzler
---
# Changelog

## [1.5.1] - Released 2019-05-20

- Added the ability to add a custom error message for `withCallback`.
- Fixed the `json_encode` formatting for the error message on `withQuery`.
- Various updates to the documentation. 

## [1.5.0] - Released 2019-05-04

- Added the `withFile` filter. Includes several new tests and a `File` helper object.
- Added the `withCallback` filter which allows users to pass an arbitrary anonymous function to filter history items.

## [1.4.2] - Released 2019-04-21

- Fix to move macros file loaded via composer. Includes test to ensure provided macros can be overridden.

## [1.4.1] - Released 2019-04-04

- Fix for possibility that Guzzler macros were not loaded because the extension may not be added to a project that was pre-existing.

## [1.4.0] - Released 2019-04-04

- Added the ability to add custom `macro`s.
- Added an `extension` class that can be added to a `phpunit.xml` file to globally load both a custom filter namespace and a macros file.

## [1.3.0] - Released 2019-03-24

- Added `Exposition::addNamespace` method to allow users to write custom filters and override Guzzler provided filters.
- Refactored `Exposition::__call` method to search through any user-provided namespaces for filters before using the defaults provided by Guzzler.

## [1.2.1] - Released 2019-03-23

- Refactored filters into class based structure so that any number of filters can be added in the future.
- Added `Disposition` class to parse multipart form post bodies.
- Refactored `WithForm` class to work with both URL encoded and multipart forms.
- Refactored `withJson` functionality to be more in-line with most other filters. Now, by default, the expectation returns true if the body contains a stringified version of the passed argument. A new `$exclusive` boolean value can be passed as the second argument to return to the previous exact match nature. The new signature is `withJson(array $json, bool $exclusive = false)`.
- Refactored `withBody` functionality to be more in-line with most other filters. Now, by default, the expectation returns true if the body contains the passed argument. A new `$exclusive` boolean value can be passed as the second argument to return to the previous exact match nature. The new signature is `withBody(string $body, bool $exclusive = false)`.

## [1.2.0] - Released 2019-03-16

- Added the new `withFormField` and `withForm` methods to the `Expectations` class.
- Added the new `withJson` method to the `Expectations` class.

## [1.1.0] - Released 2019-03-03

- Added the new `synchronous` and `asynchronous` methods to the `Expectations` class.
- Updated brand slogan to "Supercharge your unit tests that use Guzzle with a mock-like syntax."

## [1.0.1] - Released 2019-03-02

- Updated the composer.json to include license info, and pointed the main README.md to the new documentation site.

## [1.0.0] - Released 2019-02-28

- Initial Release