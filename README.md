# Makefile to Markdown

![Coverage](https://img.shields.io/badge/coverage-100%25-brightgreen)

<!-- ![Code Style](https://img.shields.io/badge/code_style-ruff-black) -->

## Overview

Simple command-line utility that converts Makefiles to Markdown if specific commenting style is followed.

### Headers

Headers (sections) should look like this:

```makefile
# -----------------------------------------------------------------------------
# Header Name
# -----------------------------------------------------------------------------
```

### Commands

Commands should look like this:

```makefile
command:  ## Command description
	echo "do something"
```

## Example Makefile

```makefile
# -----------------------------------------------------------------------------
# Testing
# -----------------------------------------------------------------------------

pytest:  ## Run tests
	uv run pytest -vx --cov --cov-report term
  uv run coverage html

pytest_verbose:  ## Run tests in verbose mode
	uv run pytest -vvs --cov --cov-report html

coverage:  ## Run tests with coverage
	uv run coverage run -m pytest && coverage html

coverage_verbose:  ## Run tests with coverage in verbose mode
	uv run coverage run -m pytest -vss && coverage html

coverage_skip:  ## Run tests with coverage and skip covered
	uv run coverage run -m pytest -vs && coverage html --skip-covered

open_coverage:  ## Open coverage report
	open htmlcov/index.html

# -----------------------------------------------------------------------------
# Ruff
# -----------------------------------------------------------------------------

ruff_format: ## Run ruff format
	uv run ruff format src/makefile_to_markdown

ruff_check: ## Run ruff check
	uv run ruff check src/makefile_to_markdown

ruff_clean: ## Run ruff clean
	uv run ruff clean
```

## Installation

```bash
python3 -m pip install makefile-to-markdown
uv add makefile-to-markdown
```

## Usage

```bash
makefile-to-markdown convert --path "Makefile"
```

## Output Example

Given the `Makefile` from the above example, it would output the following Markdown:

```md
### Testing

| Command            | Description                              |
| ------------------ | ---------------------------------------- |
| `pytest`           | Run tests                                |
| `pytest_verbose`   | Run tests in verbose mode                |
| `coverage`         | Run tests with coverage                  |
| `coverage_verbose` | Run tests with coverage in verbose mode  |
| `coverage_skip`    | Run tests with coverage and skip covered |
| `open_coverage`    | Open coverage report                     |

### Ruff

| Command       | Description     |
| ------------- | --------------- |
| `ruff_format` | Run ruff format |
| `ruff_check`  | Run ruff check  |
| `ruff_clean`  | Run ruff clean  |
```

## Development

```bash
make env
make pip_install
make pip_install_editable
```

## Testing

```bash
make pytest
make coverage
make open_coverage
```

## Issues

If you experience any issues, please create an [issue](https://github.com/tsantor/makefile-to-markdown/issues) on Github.

## Not Exactly What You Want?

This is what I want. _It might not be what you want_. If you have differences in your preferred setup, I encourage you to fork this to create your own version.
