Github action for linting the C++ code.
Uses clang-tidy.

Example of usage:
```
name: lint

on: [pull_request]
jobs:
  clang-tidy:
    name: clang-tidy
    runs-on: ubuntu-latest
    steps:
      - name: clang-tidy check
        uses: smay1613/clang-tidy-action@master
    env:
        GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```
