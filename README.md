# textlint-with-pre-commit

Mirror of textlint package for pre-commit.  
Use textlint with pre-commit.

For pre-commit: [https://github.com/pre-commit/pre-commit](https://github.com/pre-commit/pre-commit-mirror-maker)  
For textlint (v15.2.1): [https://github.com/textlint/textlint](https://github.com/textlint/textlint)

## Using textlint with pre-commit
Add this to your .pre-commit-config.yaml:

```yaml
# textlint
- repo: https://github.com/studiogadget/textlint-with-pre-commit
  rev: v15.2.1
  hooks:
    - id: textlint
      files: \.(markdown|md)$
      additional_dependencies:
        # Write npm package of rules to be used.
        - "textlint-filter-rule-comments"
        - "textlint-filter-rule-allowlist"
        - "textlint-rule-prh"
        - "textlint-rule-preset-ja-technical-writing"
```
