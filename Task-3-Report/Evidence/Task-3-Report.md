# Task 3 – Automated Testing and CI Workflow

## Objective

Script an automated testing and integration workflow running on remote pushes.

## Technologies Used

- GitHub Actions
- Python
- Flask
- Pytest
- Flake8
- GitHub

## Implementation

A GitHub Actions CI pipeline was configured to automatically run whenever code is pushed to the repository.

The workflow performs the following steps:

1. Checks out the repository code.
2. Sets up Python 3.13.
3. Installs project dependencies.
4. Runs Flake8 for static code linting.
5. Runs Pytest unit tests.
6. Displays the workflow execution status on GitHub Actions.

## Pipeline Workflow

GitHub Push → Checkout Code → Setup Python → Install Dependencies → Flake8 → Pytest → Workflow Status

## Evidence

![GitHub Actions Success](Evidence/01-GitHub-Actions-Success.png)