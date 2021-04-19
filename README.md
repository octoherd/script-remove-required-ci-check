# setup renovate

> An [octoherd](https://github.com/octoherd) script to remove a required status check from all protected branches

## Usage

```
$ npx @octoherd/script-remove-required-ci-check \
  --check "continuous-integration/travis-ci"
```

Pass all options as CLI flags to avoid user prompts

```
$ npx @octoherd/script-remove-required-ci-check \
  --check "continuous-integration/travis-ci" \
  -T ghp_0123456789abcdefghjklmnopqrstuvwxyzA \
  -R "octoherd/repository-with-script-folders"
```

## Options

| option                       | type             | description                                                                                                                                                                                                                                 |
| ---------------------------- | ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `--check`                    | string           | Name of CI integration. Example: `--check continuous-integration/travis-ci`                                                                                                                                                                 |
| `--octoherd-token`, `-T`     | string           | A personal access token ([create](https://github.com/settings/tokens/new?scopes=repo)). Script will create one if option is not set                                                                                                         |
| `--octoherd-repos`, `-R`     | array of strings | One or multiple space-separated repositories in the form of `repo-owner/repo-name`. `repo-owner/*` will find all repositories for one owner. `*` will find all repositories the user has access to. Will prompt for repositories if not set |
| `--octoherd-bypass-confirms` | boolean          | Bypass prompts to confirm mutating requests                                                                                                                                                                                                 |

## Licenses

[ISC](LICENSE.md)
