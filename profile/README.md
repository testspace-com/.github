[Testspace](https://testspace.com/) provides a **dashboard** for publishing test results from automation and a **framework** for implementing and executing manual tests using GitHub.

- Publish large volumes of test results with a single command
- Implement Manual tests using text files contained in a repository
- Improve process with metrics, graphs, and analytics
- Auto-detect Flaky tests
- Exploratory support

[LIVE DEMO](https://demo.testspace.com/)

## Publish CI Test Results
Publish large volumes of automated test results with a single command. Include code coverage, static analysis, and other important metrics.

Built-in support for branching, forks, and pull requests. Automatically aggregates test results from parallel jobs.
```
 steps:
   - uses: testspace-com/setup-testspace@v1
      with:
        domain: ${{github.repository_owner}}
     ..
   - name: Publish Results to Testspace
     run: testspace [${{ matrix.os}}]./testcontent/*.xml
```

## Implement Manual Tests as Code using GitHub
Implement manual tests as code, using text files leveraging the simplicity of markdown and the power of templates, including variables, parameters, and control logic.

Use GitHub repository branches and pull requests to manage the test content. Fully integrated test management and triaging via GitHub issues and projects.

Execute Actions and AWS Lambdas with your tests, combining automated fixturing with human observations.

## Some Reference Material

- [Documentation](https://help.testspace.com)
- [Visualizing GitHub Automated Test Results](https://www.testspace.com/blog/visualizing-test-results-with-github-actions) blog article
- [Implementing Manual Tests using GitHub Repositories](https://www.testspace.com/blog/github-test-case-management) blog article 
