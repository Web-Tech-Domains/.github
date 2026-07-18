# Branch Protection Policy

This is the default branch protection policy for repositories in the **Web Tech Domains** GitHub organization. Individual repositories should configure these rules under **Settings → Branches** and may extend them as needed.

## Protected Branches

- `main`
- `production`
- `staging` (where applicable)

## Rules

### Direct Pushes

❌ Direct pushes are not allowed.

All changes must be submitted through Pull Requests.

### Pull Requests

- Minimum 1 approval required
- All conversations must be resolved
- CI/CD checks must pass
- No force pushes

### Commit Requirements

- Use meaningful commit messages
- Follow [Conventional Commits](https://www.conventionalcommits.org/)

Examples:

```
feat: add AI chat widget
fix: resolve login validation issue
docs: update deployment guide
```

### Security

- Secret scanning enabled
- Dependency scanning enabled ([dependabot.yml](.github/dependabot.yml))
- Code review mandatory ([CODEOWNERS](.github/CODEOWNERS))

### Deployment

Only approved and tested code may be merged into `production` or `staging` branches.
