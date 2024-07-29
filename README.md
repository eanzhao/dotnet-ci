# dotnet-ci-action

## Inputs
- commit-token: A Github Token with `repos` scope.
- codecov-token: A Codecov Token to upload codecov.
- branch-name: A branch to store test results files.
- solution-name: The name of the solution(sln) file.

## What did this action do
1. Build solution
2. Run all tests where projects name end with `Tests`
3. Upload codecov.
4. Create or update test results files of specific branch for tests badges.

## Badge url
Will be like:
```
https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/{YourUserName}/{YourProjectName}/{NameOfYourBranchToStoreTestResults}/{NameOfYourBranchToShowBadge}-test-results.json
```

For instance:

![GitHub Workflow Test Status](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/eanzhao/AElf/feature/badge/master-test-results.json)
