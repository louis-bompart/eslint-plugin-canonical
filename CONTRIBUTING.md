# Contributing

## Pre-Commit Hook

When making a commit, the following Pre-Commit hooks run:

* test and documentation checks
* tests
* lint
* commit message validation (see "Commit Messages" below)

## Commit Messages

All commit messages must begin with one of the following prefixes:

* `fix: `
* `feat: `
* `refactor: `
* `docs: `
* `chore: `

The prefix is used to bump the correct segment of the version number during the automatic release.

## Tests

Run them with `npm test`.

## Lint

Run with `npm run lint`.

## Adding a Rule

### Source & Tests

1. Create a file in `tests/rules/assertions` named the `camelCase` version of your rule name with the following template:
  * `export default { invalid: [], valid: [] }`
2. Add your test file to `tests/rules/index.js`
3. Create a file in `src/rules` named the `camelCase` version  of your rule name
4. Add your rule file to `src/index.js`

Note: Sections "The following patterns are considered problems:" and "The following patterns are not considered problems:" are **generated automatically** using the test cases.
