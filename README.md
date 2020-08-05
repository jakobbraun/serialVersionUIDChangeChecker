# serialVersionUID change checker

This [pre-commit](https://pre-commit.com/) hook shows a warning if a file was changed, but serialVersionUID was not.

It blocks the commit until the serialVersionUID was changed. If a change is not required, simply add or remove an empty comment in the line of the serialVersionUID.

## Setup

Add the following lines to your `.pre-commit-config.yaml`:
```yaml
  - repo: https://github.com/jakobbraun/serialVersionUIDChangeChecker
    rev: master
    hooks:
      - id: serial-version-uid
```