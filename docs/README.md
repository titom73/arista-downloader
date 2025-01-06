<!-- [![tests](https://github.com/titom73/eos-downloader/actions/workflows/pr-management.yml/badge.svg?event=push)](https://github.com/titom73/eos-downloader/actions/workflows/pr-management.yml)
![PyPI - Python Version](https://img.shields.io/pypi/pyversions/eos-downloader)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
![Checked with mypy](http://www.mypy-lang.org/static/mypy_badge.svg)
![GitHub release](https://img.shields.io/github/v/release/titom73/arista-downloader)
![PyPI - Downloads/month](https://img.shields.io/pypi/dm/eos-downloader)
[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/pre-commit/pre-commit) -->

# Arista Software Downloader

A project to download Arista softwares to local folder, Cloudvision or EVE-NG. It comes in 2 way: a framework with object to automate Arista software download and a CLI for human activities.

<img src='imgs/readme-7.png' class="center" />

> [!CAUTION]
> This script should not be deployed on EOS device. If you do that, there is no support to expect from Arista TAC team.

```bash
# install eos-downloader from pypi
pip install eos-downloader

# download EOS swi for EOS 64bits
ardl --token <your-token> get eos --format 64 --latest --release-type M
```

## Author

From an original idea of [@Mark Rayson](https://github.com/Sparky-python) in [arista-netdevops-community/eos-scripts](https://github.com/arista-netdevops-community/eos-scripts)

## License

Code is under [Apache2](https://github.com/titom73/eos-downloader/blob/main/LICENSE) License