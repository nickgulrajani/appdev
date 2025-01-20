# Sample Project with GitHub Actions

This project demonstrates the setup of GitHub Actions for:
- Code Coverage
- Security Scanning
- Dependency Checking

## Setup

1. Clone the repository
2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scriptsctivate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Running Tests

```bash
pytest
```

## GitHub Actions

The following workflows are configured:

1. Code Coverage (`code-coverage.yml`)
   - Runs on every push and pull request
   - Generates coverage reports
   - Uploads to Codecov

2. Security Scan (`security-scan.yml`)
   - Runs security checks using multiple tools
   - Performs vulnerability scanning
   - Checks for common security issues

3. Dependency Check (`dependency-check.yml`)
   - Scans dependencies for known vulnerabilities
   - Generates detailed reports
   - Runs on a weekly schedule

## Setting Up GitHub Repository

1. Create a new repository on GitHub
2. Push this code to the repository
3. Set up required secrets:
   - Go to Repository Settings > Secrets and Variables > Actions
   - Add required secrets (e.g., SNYK_TOKEN)
4. Enable GitHub Actions:
   - Go to Repository Settings > Actions > General
   - Allow all actions and reusable workflows