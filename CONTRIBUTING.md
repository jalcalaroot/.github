# Contributing

Thanks for your interest! These repositories are personal cloud and infrastructure-as-code projects (AWS, Azure, Kubernetes) maintained by [@jalcalaroot](https://github.com/jalcalaroot). Contributions, fixes and suggestions are welcome.

## Before you start

- **Security issues:** don't open a public issue; follow [SECURITY.md](SECURITY.md).
- **Bigger changes:** open an issue first so we can agree on the approach before you invest time.
- **Legacy repos:** repositories marked *legacy reference* in their README are kept mainly for reference. Small fixes are fine, but large refactors are unlikely to be merged.

## How to contribute

1. Fork the repository and create a branch from the default branch (`feat/...`, `fix/...`, `docs/...`).
2. Keep changes focused: one topic per pull request.
3. Make sure the repository's checks pass locally where they apply:
   - Terraform: `terraform fmt -recursive` and `terraform validate`
   - Linters and scanners used in the repo (for example `tflint`, `checkov`, `pre-commit run --all-files`)
4. Open a pull request that describes **what** changed, **why**, and how you tested it (for infrastructure changes, include the relevant part of `terraform plan`).

## Ground rules for infrastructure code

- **Never commit secrets or real identifiers.** That includes access keys, passwords, tokens, AWS account IDs, Azure subscription or tenant IDs, real emails and internal domains. Use placeholders such as `<AWS_ACCOUNT_ID>` or `<TENANT_ID>`, together with variables or secret managers.
- Never commit Terraform state (`*.tfstate`), `*.tfvars` with real values, or `.terraform/` folders.
- Prefer secure defaults: least-privilege IAM, encryption at rest and in transit, and no `0.0.0.0/0` on administrative ports.
- In GitHub Actions, pin third-party actions to a full commit SHA, set minimal `permissions:`, and use OIDC instead of long-lived cloud credentials.

## Code of conduct

By participating you agree to follow the [Code of Conduct](CODE_OF_CONDUCT.md).

## License

By contributing, you agree that your contributions will be licensed under the license of the repository you contribute to (MIT for most of them).
