# Security Policy

This project is a local desktop tool that uses the official Clash Royale API. It does **not** require any server and does **not** intentionally store your API token on disk.

## Supported Versions

Security fixes are provided for the latest version on the `main` branch.

## Reporting a Vulnerability

If you believe you found a security or privacy issue, please **do not** open a public GitHub issue.

Instead, report it privately:

1. Open a GitHub private security advisory (preferred), or
2. Contact the maintainer directly (if an email is listed on the GitHub profile).

Please include:

- A clear description of the issue and impact
- Steps to reproduce (proof-of-concept if possible)
- Your OS and Python version
- Any relevant logs **with tokens removed**

## What Counts as a Security Issue Here

Examples:

- API token leakage (printed to console, logged to disk, included in crash traces)
- Storing tokens or personal data on disk without user consent
- Unintended network requests to third-party domains
- Dependency vulnerabilities that could expose credentials

## Handling of Secrets (API Token)

- Never commit API tokens to the repository.
- Do not paste tokens into issues, PRs, screenshots, or logs.
- If you believe you accidentally leaked a token, **revoke it immediately** in the Clash Royale Developer Portal and generate a new one.

## Dependency Updates

This project depends on `requests`. If a vulnerability is announced:

- Update `requests` to a patched version
- Validate the app still runs (`python -m py_compile API.py clashroyaleUI.py`)
- Prefer minimal changes unrelated to the security fix

## Responsible Disclosure

Please allow a reasonable time for investigation and a fix before publishing details publicly. We’ll do our best to respond quickly and credit reporters who want attribution.

