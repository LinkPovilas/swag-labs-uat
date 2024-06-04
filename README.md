# Swag Labs User Acceptance Tests

🎭 Playwright project example, heavily inspired by the Screenplay design pattern.

## Project structure

```Shell
.
├── activities # Steps of a business workflow in your domain
├── data       # Test data
├── decorators # TypeScript decorators
├── fixtures   # Dependency injection and state handling
├── pages      # Lean page objects
├── questions  # Methods to retrieve information about the application under test
└── tests      # Test cases
```

## Building blocks of a test scenario

![](data:image/webp;base64,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)

- **Questions** should return values.
- **Interactions** should not return values.
- **Tasks** are composed of multiple interactions and/or tasks. Should never return values.

## Tips for writting tests

1. **Create Lean Page Objects**

   Instead of creating large, monolithic page objects, describe related page elements together and keep business logic out of them. Modular components are easier to reuse and maintain.

2. **Define selectors as getter functions**

   By defining selectors as getter functions, they will not be initialized immediately. This can help handle application state changes more effectively and reduce test flakiness.

3. **Encapsulate interactions with natural language**

   Use natural language to encapsulate interactions with the application under test in command-like objects. This approach makes your code easier to understand.

4. **Use Playwright's test fixtures for dependency injection**

   Use test fixtures for dependency injection and object initialization to reduce duplication of test setup.

5. **Keep assertions on the test level**

   Assertions should be kept on the test level for better understanding of expected outcomes.

6. **Describe tests as features or components**

   Use simple and descriptive test titles that clearly state what the feature or component should allow the end-user to do.

7. **Keep the project structure flat**

   A flat project structure makes navigation easier. Consider using a tool like [this site](https://tree.nathanfriend.io/) to plan your project structure.

8. **Avoid third-party libraries**

   Be mindful of the number of libraries you introduce to your project. Not every problem requires a new dependency. A good rule of thumb is to avoid introducing third-party libraries unless absolutely necessary, as they can introduce additional maintenance and compatibility issues.

## Setup

```Shell
# Install dependencies.
npm i

# Install Playwright browsers.
npx playwright install

# Install Playwright operating system dependencies.
sudo npx playwright install-deps
```

## Running tests

```Shell
# Run the end-to-end tests.
npx playwright test

# Start the interactive UI mode.
npx playwright test --ui

# Run the tests in debug mode.
npx playwright test --debug
```

## References

- [Lean Page Objects](https://johnfergusonsmart.com/page-objects-that-suck-less-tips-for-writing-more-maintainable-page-objects/)
- [Using Getters](https://webdriver.io/docs/pageobjects/#get--ing-your-selectors)
- [Screenplay Pattern](https://serenity-js.org/handbook/design/screenplay-pattern/)
- [Playwright Test Fixtures](https://playwright.dev/docs/test-fixtures)
