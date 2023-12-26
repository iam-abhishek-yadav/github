# Using GitHub Actions

GitHub Actions allows us to automate various tasks and workflows in the repository.

## Steps to Set Up and Use GitHub Actions

### 1. Create a Workflow File

1. Create a `.github/workflows` directory at the root of the repository if it doesn't already exist.
2. Inside the `.github/workflows` directory, create a YAML file for the workflow. This file defines the steps and actions that the workflow will perform.

### 2. Define Workflow

In this repo, it is defined as follows:

```yaml
name: Run Tests

on:
  push:
    branches:
      - main
  pull_request:

jobs:
  test:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repository
        uses: actions/checkout@v2

      - name: Set up Python
        uses: actions/setup-python@v3
        with:
          python-version: 3.8

      - name: Run tests
        run: python github_actions/test.py
```

### 3. Push Changes

Save the workflow file and commit it to the repository.

### 4. View Github Actions in Action

GitHub Actions will now automatically run defined workflow whenever changes are pushed repository. To view the status and logs of workflow, visit the "Actions" tab in the repository.

For more: [GitHub Starter Workflows](https://github.com/actions/starter-workflows) [GitHub Actions Quickstart](https://docs.github.com/en/actions/quickstart)
