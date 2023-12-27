# Pre-commit

`pre-commit` can be used to automatically run selene using git hooks. Once you have [pre-commit installed](https://pre-commit.com/#install), add one of the following configuration to your `.pre-commit-config.yaml` file:

1. If you want to use the `selene` binary available on your system path
```yaml
repos:
  - repo: https://github.com/Kampfkarren/selene
    rev: ''
    hooks:
      - id: selene-system
```
2. If you want to use `selene` using the available docker image
```yaml
repos:
  - repo: https://github.com/Kampfkarren/selene
    rev: ''
    hooks:
      - id: selene-docker
```
3. If you want to use `selene` using the GitHub releases
```yaml
repos:
  - repo: https://github.com/Kampfkarren/selene
    hooks:
      - id: selene-github
```