[Testspace](https://www.testspace.com) is test management for large automated test suites. Publish test results from any CI, see which failures are new, which tests are flaky and which keep failing, and know month by month whether quality is getting better. Manual tests run beside the automated results.

**[Explore the live demo](https://s2.testspace.com/projects/EXAMPLE:RESULTS)**: no account needed.

## Publish test results from GitHub Actions

```yml
steps:
  - uses: actions/checkout@v4
  - uses: testspace-com/setup-testspace@v1
    with:
      domain: ${{ github.repository_owner }}
  # ... build and run your tests ...
  - run: testspace "test-results/*.xml" coverage.xml
    if: always()
```

Each branch and pull request gets its own results, parallel and matrix jobs combine into one, and Health posts a status check on every commit. See [Visualizing GitHub Actions test results](https://www.testspace.com/blog/visualizing-test-results-with-github-actions).

## Manual tests kept in GitHub

Specs are Markdown with Liquid, changed through commits and pull requests like the code, and run by testers in Testspace test sessions; a failed case can open a GitHub issue. See [Implementing manual tests using GitHub repositories](https://www.testspace.com/blog/github-test-case-management).

## In this organization

- [setup-testspace](https://github.com/testspace-com/setup-testspace): the GitHub Action that installs and configures the Testspace client ([Marketplace](https://github.com/marketplace/actions/testspace-setup-cli))
- [cypress-xml-reporter](https://github.com/testspace-com/cypress-xml-reporter): a JUnit XML reporter for Cypress with screenshots, videos and logs
- [demo](https://github.com/testspace-com/demo): an example of manual tests kept in GitHub
- [example-cypress.xml.reporter](https://github.com/testspace-com/example-cypress.xml.reporter) and [example-jest.puppeteer.screenshots](https://github.com/testspace-com/example-jest.puppeteer.screenshots): examples for the Cypress and Jest guides
- [support](https://github.com/testspace-com/support): questions, bugs and feature requests

## More

[Testspace on the GitHub Marketplace](https://github.com/marketplace/testspace-com) · [Documentation](https://help.testspace.com) · [Guides](https://www.testspace.com/blog) · [Pricing](https://www.testspace.com/pricing)
