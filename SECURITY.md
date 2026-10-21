# Security Policy

This policy applies to every repository under [github.com/jalcalaroot](https://github.com/jalcalaroot) that does not define its own `SECURITY.md`.

## Supported versions

These repositories are personal reference implementations, proofs of concept and infrastructure-as-code templates. Only the default branch (`main` or `master`) receives fixes. Repositories marked **legacy reference** in their README are kept for reference and may not be patched; use them as a starting point, not as production-ready code.

## Reporting a vulnerability

**Please do not open a public issue for security problems.**

Report it privately through GitHub instead:

1. Go to the affected repository.
2. Open the **Security** tab and click **Report a vulnerability**.
3. Describe the issue, the affected file(s) or resource(s), how to reproduce it, and the potential impact.

This creates a private advisory that only the maintainer can see.

Please include:

- Repository and commit or branch
- Steps to reproduce or a proof of concept
- Impact (for example credential exposure, privilege escalation or data exposure)
- Any suggested fix

## What to expect

- Acknowledgement within **7 days**
- An initial assessment and next steps within **14 days**
- Credit in the fix or advisory if you want it

## Scope

In scope:

- Secrets, credentials or sensitive identifiers committed to a repository
- Insecure defaults in Terraform, CloudFormation, Bicep or Kubernetes code that would expose resources when deployed as documented
- Vulnerabilities in CI/CD workflows, such as injection, excessive token permissions or unsafe OIDC trust

Out of scope:

- Findings in third-party dependencies with no demonstrated impact on these repositories (report those upstream)
- Intentionally vulnerable code that is clearly labelled as a security-testing lab
- Risky defaults in legacy templates that are already documented in their README's *Security notes* section
