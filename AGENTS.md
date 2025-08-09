<general_rules>

- Before creating new functions or modules, search the `src` directory to see if similar functionality already exists.
- Use the provided npm scripts for common development tasks:
  - `yarn format`: Formats the code using Prettier.
  - `yarn format:check`: Checks for formatting issues.
  - `yarn lint`: Lints the code using ESLint.
  - `yarn lint:fix`: Automatically fixes linting issues.
- The CI pipeline enforces formatting and linting rules on all pull requests.
  </general_rules>
  <repository_structure>
- The main application entry point is `src/index.ts`.
- All TypeScript source code is located in the `src` directory.
- Compiled JavaScript files are output to the `dist` directory.
- GitHub Actions workflows for CI/CD are located in `.github/workflows`.
- Helper scripts for development and CI are in the `scripts` directory.
  </repository_structure>
  <dependencies_and_installation>
- This project uses `yarn` as the package manager.
- To install dependencies, run `yarn install`.
- The CI environment uses `yarn install --immutable` to ensure reproducible builds.
  </dependencies_and_installation>
  <testing_instructions>
- The project uses Jest for both unit and integration testing.
- Test files are located in the `src` directory and follow the naming convention `*.test.ts` for unit tests and `*.int.test.ts` for integration tests.
- Run unit tests with the `yarn test` command.
- Run integration tests with the `yarn test:int` command.
- The Jest configuration is defined in `jest.config.js`.
  </testing_instructions>
  <pull_request_formatting>
- Pull request titles must follow the Conventional Commits specification.
- A GitHub Action (`.github/workflows/pr_lint.yml`) lints PR titles.
