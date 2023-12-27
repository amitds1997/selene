To integrate selene with git, you can use [pre-commit](https://pre-commit.com). Once you have [pre-commit installed](https://pre-commit.com/#install), add this to the `.pre-commit-config.yaml` at root of your repository:
```yaml
repos:
  - repo: https://github.com/Kampfkarren/selene
    rev: '' # Change this value to use a different version of Selene
    hooks:
      - id: selene-system # Use the selene binary already present on system path
      - id: selene-docker # To use docker to run the hook, needs docker to be present
```
You need to mention only one of the two hooks ids depending upon if you already have the binary available or not on your system path.