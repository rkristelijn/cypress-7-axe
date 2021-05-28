# Cypress version 7 versus cypress-axe

Test repo for testing out Cypress 7 with cypress-axe for accessibility testing

## Usage

- `npm i` - to install dependencies

Then:

1. `npm start` - to run Cypress in interactive mode
2. `npm test` - to run Cypress in headless mode

## Log

- create new repo, `npm i cypress`, let Cypress set up the folders
- install cypress-axe `npm i -D cypress-axe --force`

When updating `cypress/plugin/index.js`:

- adding `import 'cypress-axe'`

```
The plugins file is missing or invalid.

Your `pluginsFile` is set to `/Users/nlrxk0145/github/cypress-7-axe/cypress/plugins/index.js`, but either the file is missing, it contains a syntax error, or threw an error when required. The `pluginsFile` must be a `.js`, `.ts`, or `.coffee` file.

Or you might have renamed the extension of your `pluginsFile`. If that's the case, restart the test runner.

Please fix this, or set `pluginsFile` to `false` if a plugins file is not necessary for your project.

 /Users/nlrxk0145/github/cypress-7-axe/cypress/plugins/index.js:1
import 'cypress-axe'
^^^^^^

SyntaxError: Cannot use import statement outside a module
    at wrapSafe (internal/modules/cjs/loader.js:986:16)
```

- adding `require('cypress-axe')`:

```
The plugins file is missing or invalid.

Your `pluginsFile` is set to `/Users/nlrxk0145/github/cypress-7-axe/cypress/plugins/index.js`, but either the file is missing, it contains a syntax error, or threw an error when required. The `pluginsFile` must be a `.js`, `.ts`, or `.coffee` file.

Or you might have renamed the extension of your `pluginsFile`. If that's the case, restart the test runner.

Please fix this, or set `pluginsFile` to `false` if a plugins file is not necessary for your project.

 ReferenceError: Cypress is not defined
```

- when importing directly in the test, it seems to work, added tasks per cypress-axe documentation