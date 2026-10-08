# Contributing to django-visit-insights

Thanks for your interest in contributing! This document outlines the basics.

## Ways to Contribute

- 🐛 **Report bugs** — open an issue with clear steps to reproduce.
- 💡 **Suggest features** — open an issue describing the use case.
- 📝 **Improve docs** — fix typos, clarify explanations, add examples.
- 🧪 **Write tests** — more coverage is always welcome.
- 🔧 **Submit code** — fix a bug or implement a feature.

## Getting Started

1. Fork the repository.
2. Clone your fork locally.
3. Create a virtual environment and install dependencies:

   ```bash
   python -m venv .venv
   source .venv/bin/activate
   pip install -e ".[dev]"
   ```

4. Create a branch for your work:

   ```bash
   git checkout -b feat/short-description
   ```

## Development Guidelines

- Follow [PEP 8](https://peps.python.org/pep-0008/).
- Write clear commit messages (see below).
- Keep pull requests focused — one change per PR.
- Add tests for new features and bug fixes.
- Update the README or CHANGELOG if needed.

## Commit Messages

Use short, imperative messages. Examples:

```
feat: add memcached backend
fix: handle missing session key in dedup
docs: clarify flush command usage
```

Prefixes: `feat`, `fix`, `docs`, `test`, `refactor`, `chore`.

## Pull Requests

- Describe what changed and why.
- Reference related issues (e.g. `Closes #12`).
- Make sure tests pass before submitting.
- Be open to feedback during review.

## Code of Conduct

Be respectful. Be kind. Assume good intentions. We're all here to build something useful together.

## Questions?

Open an issue or start a discussion — happy to help.
