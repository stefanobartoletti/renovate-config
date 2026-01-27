# renovate-config

Personal shareable Renovate config extending Nuxt config without grouping all non-major updates.

## What it does

This configuration:

- Extends both `config:recommended` and `github>nuxt/renovate-config-nuxt`
- Overrides the `group:allNonMajor` behavior from the Nuxt config
- Creates separate PRs for each minor and patch update instead of grouping them all together

## Usage

### Option 1: Using GitHub reference (recommended for personal use)

Add this to your `renovate.json`:

```json
{
  "extends": ["github>stefanobartoletti/renovate-config"]
}
```

### Option 2: Using npm package

If published to npm, you can use:

```json
{
  "extends": ["@stefanobartoletti/renovate-config"]
}
```

## Why this config?

The Nuxt Renovate config includes `group:allNonMajor` which groups all minor and patch updates into a single PR. While this reduces the number of PRs, it can make it harder to review and test individual dependency updates. This configuration disables that grouping behavior while keeping all other Nuxt-specific settings.

## License

MIT
