# renovate-config

Shared [Renovate](https://docs.renovatebot.com/) preset for **JorisJonkers-dev** repositories.

Every repo in the org extends this preset from its own `renovate.json`:

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>JorisJonkers-dev/renovate-config"]
}
```

## What `default.json` provides

- `config:recommended` + semantic commits + a dependency dashboard.
- `rangeStrategy: pin`, a 7-day `minimumReleaseAge`, weekly lock-file maintenance.
- Routine minor/patch grouped; majors require dashboard approval.
- First-party **JorisJonkers-dev** artifacts (npm `@jorisjonkers-dev/*`, Maven `dev.jorisjonkers`,
  `ghcr.io/jorisjonkers-dev/*`, the shared GitHub Actions repos) grouped into one coherent platform bump.
- Legacy **ExtraToast** coordinates are **disabled** during the migration cutover — they are renamed by the
  migration, not auto-bumped.
- GitHub Actions pinned to immutable digests.
- Flux/Kustomize image-tag managers for the `homelab-deploy` GitOps tree (pinned `ghcr.io/jorisjonkers-dev`
  semver tags), labelled for the deploy gate.

Maintained as part of the ExtraToast → JorisJonkers-dev migration (see `migration/` runbook).
