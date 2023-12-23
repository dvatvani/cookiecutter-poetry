<p align="center">
  <img width="600" src="https://raw.githubusercontent.com/dvatvani/cookiecutter-poetry/main/docs/static/cookiecutter.svg">
</p style = "margin-bottom: 2rem;">

---

[![Release](https://img.shields.io/github/v/release/dvatvani/cookiecutter-poetry)](https://pypi.org/project/cookiecutter-poetry/)
[![Build status](https://img.shields.io/github/actions/workflow/status/dvatvani/cookiecutter-poetry/main.yml?branch=main)](https://github.com/dvatvani/cookiecutter-poetry/actions/workflows/main.yml?query=branch%3Amain)
[![Supported Python versions](https://img.shields.io/pypi/pyversions/cookiecutter-poetry)](https://pypi.org/project/cookiecutter-poetry/)
[![Docs](https://img.shields.io/badge/docs-gh--pages-blue)](https://dvatvani.github.io/cookiecutter-poetry/)
[![License](https://img.shields.io/github/license/dvatvani/cookiecutter-poetry)](https://img.shields.io/github/license/dvatvani/cookiecutter-poetry)

This is a modern Cookiecutter template that can be used to initiate a Python project with all the necessary tools for development, testing, and deployment. It supports the following features:

- [Poetry](https://python-poetry.org/) for dependency management
- CI/CD with [GitHub Actions](https://github.com/features/actions)
- Pre-commit hooks with [pre-commit](https://pre-commit.com/)
- Code quality with [ruff](https://github.com/charliermarsh/ruff), [mypy](https://mypy.readthedocs.io/en/stable/), [deptry](https://github.com/fpgmaas/deptry/) and [prettier](https://prettier.io/)
- Publishing to [Pypi](https://pypi.org) or [Artifactory](https://jfrog.com/artifactory) by creating a new release on GitHub
- Testing and coverage with [pytest](https://docs.pytest.org/en/7.1.x/) and [codecov](https://about.codecov.io/)
- Documentation with [MkDocs](https://www.mkdocs.org/)
- Compatibility testing for multiple versions of Python with [Tox](https://tox.wiki/en/latest/)
- Containerization with [Docker](https://www.docker.com/)
- Development environment with [VSCode devcontainers](https://code.visualstudio.com/docs/devcontainers/containers)

---

<p align="center">
  <a href="https://dvatvani.github.io/cookiecutter-poetry/">Documentation</a> - <a href="https://github.com/dvatvani/cookiecutter-poetry-example">Example</a> -
  <a href="https://pypi.org/project/cookiecutter-poetry/">PyPi</a>
</p>

---

## Quickstart

On your local machine, navigate to the directory in which you want to
create a project directory, and run the following commands:

```bash
pip install cookiecutter
cookiecutter gh:dvatvani/cookiecutter-poetry
```

To set the project up, create a new project on GitHub with the same name (do not create any of the automatic files), then navigate into the project directory and run the `setup-project` justfile recipe as follows:

```bash
cd <project_name>
just setup-project
```

That will initialise the Git repository, install the poetry environment, and push the first commit to GitHub to establish the remote location. If you prefer to skip setting up the GitHub project for now, you can instead run `just setup-project-no-github`.

You are now ready to start development on your project! The CI/CD
pipeline will be triggered when you open a pull request, merge to main,
or when you create a new release.

To finalize the set-up for publishing to PyPi or Artifactory, see
[here](https://dvatvani.github.io/cookiecutter-poetry/features/publishing/#set-up-for-pypi).
For activating the automatic documentation with MkDocs, see
[here](https://dvatvani.github.io/cookiecutter-poetry/features/mkdocs/#enabling-the-documentation-on-github).
To enable the code coverage reports, see [here](https://dvatvani.github.io/cookiecutter-poetry/features/codecov/).

## Acknowledgements

This is a fork of [fpgmaas' excellent cookiecutter template](https://github.com/fpgmaas/cookiecutter-poetry). The key changes implemented in this fork compared to the original are:

- Use of justfile instead of Makefile to streamline common dev tasks
- Projects created with this template use the [src layout](https://packaging.python.org/en/latest/discussions/src-layout-vs-flat-layout/) rather than the flat layout used in the original project.
- Includes fully automated API reference docs generation from Google-style docstrings in the code.
