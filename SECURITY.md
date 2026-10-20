# Security Policy

Thank you for helping keep igorski's open-source projects secure. Because many of these projects run entirely client-side, it's important to protect users from malicious scripts, Cross-Site Scripting (XSS), and dependency exploits. 

Please read the guidelines below regarding security vulnerabilities and contribution rules across the repositories.

## Supported Versions

igorski actively supports and patches only the latest release of the projects. If you find a bug or vulnerability in an older version, please verify if it persists in the latest release before reporting.

**Maintenance & Updates:** As the sole maintainer, igorski monitors security developments and dependencies, performing periodic updates and maintenance across repositories as needed.

## Reporting a Vulnerability

If you discover a security vulnerability, please **do not open a public GitHub issue or comment**. 

Instead, please use the official **GitHub Private Vulnerability Reporting** feature:
1. Navigate to the main page of the specific repository where you found the issue.
2. Click on the **Security** tab below the repository name.
3. Click on **Advisories** in the left sidebar.
4. Click **Report a vulnerability** to open a private advisory form directly with the maintainer.

This keeps the discussion completely private until a patch is ready.

## Contribution Security Rules

To ensure the safety of the projects, a zero-trust policy is enforced for external pull requests _across all repositories_. Any contribution that violates the following rules will be rejected:

* **No Obfuscation:** All code must be human-readable, clear, and easy to audit. Minified code, hidden logic, or unusual string encodings (such as encoded hexadecimal or base64 payloads) in Pull Requests are prohibited.
* **No Unsolicited Dependency Updates:** Do not modify package manager files (e.g., `package.json`, `package-lock.json`, `Cargo.toml`, etc.) or introduce new external third-party libraries unless explicitly requested or approved in an open issue beforehand.
* **No External Resources:** Pull requests must not introduce code that fetches external scripts, tracking pixels, or assets dynamically at runtime.

If a Pull Request contains suspicious, unreadable, or unapproved dependency changes, it will be closed immediately.
