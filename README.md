# Terraform Security Checks for AWS with GitHub Actions

This repository includes a GitHub Actions workflow to run security checks using Bandit, Terrascan, Checkov, and Snyk. The workflow is triggered on each push and pull request to ensure continuous security monitoring of the codebase.

## Prerequisites

1. **GitHub Repository**: Ensure you have a GitHub repository where you want to set up the security checks.
2. **Snyk Account**: Create an account on [Snyk](https://snyk.io/) to obtain an API token.

## Setup Instructions

1. **Add the Workflow File**:
   - Ensure the `security-checks.yml` file is located in the `.github/workflows` directory of your repository.

2. **Set Up Snyk Token**:
   - Go to your GitHub repository.
   - Click on `Settings` > `Secrets and variables` > `Actions`.
   - Click on `New repository secret`.
   - Add a new secret with the name `SNYK_TOKEN` and your Snyk API token as the value.

## Running the Workflow

The GitHub Actions workflow will automatically run on each push and pull request to the repository. It will perform the following security checks:
- **Bandit**: Checks for security issues in Python code.
- **Terrascan**: Checks for security issues in Infrastructure as Code (IaC) configurations.
- **Checkov**: Checks for security issues in Terraform configurations.
- **Snyk**: Checks for vulnerabilities in the code and dependencies.
- **Timeout Check**: Ensures all HTTP requests have a timeout specified.

## Viewing Reports

The results of each security check are uploaded as artifacts in the GitHub Actions workflow run. You can download and review these reports to identify and fix security issues in your codebase.

## Contributing

If you have suggestions or improvements for this workflow, feel free to open an issue or submit a pull request.

## License

This project is licensed under the MIT License.
