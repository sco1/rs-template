# rs-template
This template is rendered with [`cargo-generate`](https://github.com/cargo-generate/cargo-generate) (`cargo install cargo-generate`). This README is only shown for the template repository itself and is not included in generated projects.

## Usage
### Using `cargo generate`
```
cargo generate sco1/rs-template
```

### Using GitHub's "Use this template"
Repositories created from GitHub's UI are a verbatim copy of the template, so the placeholders still need to be rendered. From the root of the cloned repository:

```
cargo generate --path . --init --overwrite --name <repository-name>
```

Then remove the template-only files:

```
git rm cargo-generate.toml .github/README.md
```

**NOTE:** `--name` should match the GitHub repository name, as it is also used for the repository & badge URLs.

## Placeholders
| Placeholder           | Used In                                  | Source                    |
|-----------------------|------------------------------------------|---------------------------|
| `{{project-name}}`    | `Cargo.toml`, `Cargo.lock`, `README.md`  | `--name` / prompt         |
| `{{description}}`     | `Cargo.toml`, `README.md`                | `--define` / prompt       |
| `{{msrv}}`            | `Cargo.toml`                             | `--define` / prompt       |
| `{{ "now" \| date }}` | `LICENSE`                                | Year of generation        |
