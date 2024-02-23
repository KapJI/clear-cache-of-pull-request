# clear-cache-by-prefix-action

A Github action to delete the cache whose key starts with a specific prefix.
This can be useful to clear the cache of a feature branch after it is merged for example.

## Usage

```yaml
On:
  pull_request:
    types: [closed]
permissions:
  actions: write
jobs:
  clear-caches:
    runs-on: ubuntu-latest
    steps:
      - name: Clear caches
        uses: theAngularGuy/clear-cache-by-prefix-action@v1.0.0
        with:
          github-token: ${{ secrets.GITHUB_TOKEN }}
          cache-prefix: my-feature-branch-
```

## Inputs

| Name                 | Description                            | Required | Default |
|----------------------|----------------------------------------|----------|---------|
| github-token         | The GitHub token to use                | Yes      | none    |
| cache-prefix         | The prefix of the cache keys to delete | Yes      | none    |

## Outputs

None.

## Contributing

Contributions to enhance the Composite action are welcome. If you find issues or have suggestions for improvements, please open an issue or submit a pull request.