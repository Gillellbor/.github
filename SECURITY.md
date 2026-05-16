# Security Policy

## Reporting a Vulnerability

If you discover a security vulnerability, please report it **privately**. Do NOT open a public GitHub issue for security vulnerabilities.

### Preferred channels

1. **GitHub Private Vulnerability Reporting** — use the "Report a vulnerability" button in the Security tab of the affected repository. This is the safest and most discoverable path.
2. **Email** — `security@hradni.net` (PGP key on request).

### Response commitment

I will acknowledge your report within **72 hours** and provide a more detailed response within **7 days** indicating the next steps.

## Supported Versions

These projects follow a rolling-release model. Only the latest release on `main` receives security updates.

## Scope

**In scope:**

- Code in this repository
- Configuration files committed to this repository (workflows, Renovate, Docker, deploy scripts)

**Out of scope:**

- Third-party services and dependencies (please report to upstream maintainers directly)
- Social engineering of repository owner or contributors
- Physical security
- Issues requiring privileged access already obtained through other means

## Public disclosure

I will coordinate public disclosure with you after the vulnerability is fixed and users have had reasonable time to update. Standard embargo: **90 days** unless extension is mutually agreed.

## Acknowledgements

Researchers who report valid vulnerabilities will be credited in the fix's release notes unless they prefer anonymity.
