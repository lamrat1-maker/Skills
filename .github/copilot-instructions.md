# Copilot cloud-agent instructions

## Repository overview

This is currently a documentation-only repository. The only project file is
`README.md`, whose complete contents are the heading `# Skills`. There is no
application, library, executable, dependency manifest, source tree, or test
suite yet. The repository is therefore language- and runtime-agnostic.

The repository root is intentionally minimal:

```text
README.md
.github/copilot-instructions.md
```

No nested project directories, generated files, or external services are
present. Keep changes similarly focused unless the task explicitly adds a new
project component. Update `README.md` when introducing user-facing behavior or
usage instructions.

## Build, test, and validation

There are no bootstrap, build, run, lint, format, or CI workflows configured.
Do not invent a package-manager setup or install dependencies for a
documentation-only change. There is no required runtime or toolchain version.

Before changing the repository, inspect the current status:

```bash
cd /home/runner/work/Skills/Skills
git status --short
```

For documentation-only changes, validate that the intended files exist, the
Markdown is readable, and no unrelated files were created:

```bash
git diff --check
git status --short
```

The following standard commands were checked and are **not applicable** here:
`make` (no Makefile), `npm test` (no `package.json`), `cargo test` (no
`Cargo.toml`), `go test ./...` (no Go module), and `python -m pytest` (pytest
is unavailable and no Python project exists). Do not treat those failures as
repository defects. If a future change adds a project manifest or workflow,
follow that project's documented commands and update these instructions.

There are currently no pre-commit checks or GitHub Actions checks to replicate.
Use `git diff --check` as the available whitespace/error check, and review the
final diff manually. Always confirm that only files relevant to the task are
modified.

## Working guidance

- Treat this file and the existing README as the authoritative repository
  guidance; search the repository only if these instructions are incomplete or
  demonstrably incorrect.
- Preserve the repository's minimal scope and avoid adding dependencies,
  generated artifacts, or tool configuration without a concrete requirement.
- Keep Markdown concise and use standard GitHub-flavored Markdown.
- For any future code or project addition, first identify its manifest,
  toolchain, entry points, tests, and CI configuration, then document and
  validate the corresponding commands here.
