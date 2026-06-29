# renovate-config

Shared Renovate preset for JorisJonkers-dev repositories.

## What It Is

`renovate-config` provides the default Renovate policy for org repositories:
semantic commits, dependency dashboards, pinned ranges, grouped first-party
updates, deploy-v2 source pin handling, and guardrails for migration-era
coordinates.

## Use

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>JorisJonkers-dev/renovate-config"]
}
```

## Local Validation

```bash
python3 -m json.tool default.json >/dev/null
npx --yes --package renovate renovate-config-validator default.json renovate.json
```

## Links

- [Organization profile](https://github.com/JorisJonkers-dev)
- [Security policy](https://github.com/JorisJonkers-dev/.github/security/policy)
- [License](./LICENSE)

Copyright (c) Joris Jonkers. Source available for viewing only; use, copying,
modification, redistribution, deployment, or reuse is not licensed. See
[LICENSE](./LICENSE).
