# graphene-django-precommit-hook
pre-commit hook to generate .graphql/.json graphql schema for [graphene-django](https://github.com/graphql-python/graphene-django).


## As a pre-commit hook

See [pre-commit](https://github.com/pre-commit/pre-commit) for instructions

Sample `.pre-commit-config.yaml`

```yaml
-   repo: https://github.com/jackton1/graphene-django-precommit-hook
    rev: v0.1.0
    hooks:
      - id: graphene-django-precommit-hook
        stages: [commit]
        args: [
          '--python-version',
          '3.6', # Defaults to: 3.6
          '--managepy-path',
          '/path/to/manage.py', # Defaults to: manage.py
          '--settings',
          'project.settings' # Defaults to: DJANGO_SETTINGS_MODULE
        ]
```