# Gillellbor/.github

Default community health files and shared automation configs for all repos under [@Gillellbor](https://github.com/Gillellbor).

## Renovate config preset

`default.json` is the shared [Renovate](https://docs.renovatebot.com/) config preset for personal projects. Any repo can use it by adding a three-line `renovate.json`:

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["local>Gillellbor/.github"]
}
```

Change the preset once here, every consuming repo picks it up automatically.

### What the preset does

- **Weekly cadence:** non-security PRs land Monday mornings (Europe/Prague).
- **Security:** vulnerability alerts get top priority, run any time, dedicated `security` label.
- **Auto-merge:** patch updates (any dep type) and devDependencies patch+minor auto-merge on green CI.
- **Grouped PRs:** Next.js + React core, Radix UI, Tailwind ecosystem, Supabase clients, linters/formatters — each grouped into one PR instead of many.
- **GitHub Actions:** pinned to full SHA (post-CVE-2025-30066 tj-actions hardening).
- **Lock file maintenance:** monthly refresh.
- **`minimumReleaseAge: 3 days`** on npm — avoids the supply-chain trap of merging a version published 30 minutes ago.

### Per-repo overrides

A consuming repo can override individual rules in its own `renovate.json`:

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["local>Gillellbor/.github"],
  "schedule": ["before 9am on tuesday"],
  "packageRules": [
    { "matchPackageNames": ["next"], "automerge": false }
  ]
}
```

## Profile

`profile/README.md` is rendered on the GitHub profile page at [github.com/Gillellbor](https://github.com/Gillellbor).
