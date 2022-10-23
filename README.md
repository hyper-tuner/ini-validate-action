# HyperTuner INI validate

GitHub Action for INI validation.

## Usage

`.github/workflows/validate-ini.yml`

```yaml
name: Validate INI

on: pull_request

jobs:
  validate:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout
        uses: actions/checkout@v2
      - name: Validate INI
        uses: hyper-tuner/ini-validate-action@v1
        with:
          github-token: "${{ secrets.GITHUB_TOKEN }}"
          filename: data/my_ini_file.ini
```
