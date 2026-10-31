# repository-template

The starting point for my new repositories: community files, issue templates, Dependabot, and GitHub Actions that check the code, docs and configuration using the shared configurations in [fharper/gh-configs](https://github.com/fharper/gh-configs).

## After creating a repository from it

1. Delete the workflows the project doesn't need (see below).
2. Replace the [license](LICENSE) if the project needs a different one.
3. If you keep `update-license.yml`, turn on **Settings → Actions → General → Allow GitHub Actions to create and approve pull requests**. It's off by default and settings aren't copied from a template.
4. Replace this README.

## Workflows

| Workflow | Checks | Delete when the project has no… |
| --- | --- | --- |
| `check-css.yml` | CSS with stylelint | CSS |
| `check-docker.yml` | Dockerfile with hadolint | Dockerfile (it skips itself, so it can stay) |
| `check-json.yml` | JSON syntax | JSON |
| `check-nodejs.yml` | JavaScript with ESLint and neostandard | Node.js project |
| `check-svg.yml` | SVG files | SVG |
| `check-terraform.yml` | Terraform with TFLint | Terraform |
| `update-license.yml` | Copyright year in the license | Year in its license |

The other workflows apply to every repository: commit messages, signed commits, issue labels and assignment, Markdown, links, spelling and style, YAML, GitHub Actions and GitHub configuration.
