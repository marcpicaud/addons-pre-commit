#PS-Addons-pre-commit

## Requirements
- [Yelp's pre-commit framework](https://github.com/pre-commit/pre-commit)
- [PHP](https://github.com/php/php-src)
- [PHP Code sniffer](https://github.com/squizlabs/PHP_CodeSniffer)

## Setup
Add a file called `.pre-commit-config.yaml` to the root of your project, with the following :
```yaml
- repo: git@github.com:/marcpicaud/addons-pre-commit.git
  sha: master
  hooks:
  - id: php-lint-all
  - id: php-cs
    files: \.(php)$
    args: [--standard=PSR2 -p]
```

then run `pre-commit install` to add the hooks.

