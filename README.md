# repository-template

The starting point for my new repositories: community files, issue templates, Dependabot, and GitHub Actions that check the code, docs and configuration using the shared configurations in [fharper/gh-configs](https://github.com/fharper/gh-configs).

## After creating a repository from it

1. Delete the workflows the project doesn't need (see below).
2. Replace the [license](LICENSE) if the project needs a different one.
3. If you keep `update-license.yml`, turn on **Settings → Actions → General → Allow GitHub Actions to create and approve pull requests**. It's off by default and settings aren't copied from a template.
4. Replace this README.

## Workflows

These fail with a message naming the file to delete when the project has none of what they check:

| Workflow | Checks | Delete when the project has no… |
| --- | --- | --- |
| `check-css.yml` | CSS with stylelint | CSS (also delete `.tools/stylelint/`) |
| `check-docker.yml` | Dockerfile with hadolint | Dockerfile (also delete `.tools/hadolint/` and the `docker` entry in `.github/dependabot.yml`) |
| `check-json.yml` | JSON syntax | JSON |
| `check-nodejs.yml` | JavaScript with ESLint and neostandard | `package.json` (also delete `.tools/eslint/`) |
| `check-svg.yml` | SVG files against SVG 1.1, which needs the XML declaration and SVG 1.1 DOCTYPE | SVG |
| `check-terraform.yml` | Terraform with TFLint | Terraform |
| `check-zsh.yml` | zsh scripts with `zsh -n` and ZShellCheck | zsh scripts (also delete `.tools/zshellcheck/` and its line in the `gomod` entry of `.github/dependabot.yml`) |
| `update-license.yml` | Copyright year in the license | Year in its license |

The other workflows apply to every repository: commit messages, signed commits, issue labels and assignment, Markdown, links, spelling and style, YAML, GitHub Actions and GitHub configuration.
