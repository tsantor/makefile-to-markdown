## Makefile Commands

### Environment

| Command | Description |
| --- | --- |
| `env` | Create virtual environment (uses `pyenv`) |
| `env_remove` | Remove virtual environment |
| `env_from_scratch` | Create environment from scratch |
| `rehash` | Rehash pyenv |

### Pip

| Command | Description |
| --- | --- |
| `pip_install` | Install requirements |
| `pip_install_editable` | Install in editable mode |
| `pip_list` | Run pip list |
| `pip_freeze` | Run pipfreezer |
| `pip_checker` | Run pipchecker |

### Testing

| Command | Description |
| --- | --- |
| `pytest` | Run tests |
| `pytest_verbose` | Run tests in verbose mode |
| `coverage` | Run tests with coverage |
| `coverage_verbose` | Run tests with coverage in verbose mode |
| `coverage_skip` | Run tests with coverage and skip covered |
| `open_coverage` | Open coverage report |

### Ruff

| Command | Description |
| --- | --- |
| `ruff_format` | Run ruff format |
| `ruff_check` | Run ruff check |
| `ruff_clean` | Run ruff clean |

### Cleanup

| Command | Description |
| --- | --- |
| `clean_build` | Remove build artifacts |
| `clean_pyc` | Remove python file artifacts |
| `clean` | Remove all build and python artifacts |
| `clean_pytest_cache` | Clear pytest cache |
| `clean_ruff_cache` | Clear ruff cache |
| `clean_tox_cache` | Clear tox cache |
| `clean_coverage` | Clear coverage cache |
| `clean_tests` | Clear pytest, ruff, tox, and coverage caches |

### Miscellaneous

| Command | Description |
| --- | --- |
| `tree` | Show directory tree |

### Deploy

| Command | Description |
| --- | --- |
| `dist` | Builds source and wheel package |
| `release_test` | Upload package to pypi test |
| `release` | Package and upload a release |
| `check` | Twine check |

### X Studios S3 PyPi

| Command | Description |
| --- | --- |
| `create_latest_copy` | Create latest copy of distro |

### Project Specific

| Command | Description |
| --- | --- |
