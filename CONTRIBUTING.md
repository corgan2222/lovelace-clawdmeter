# Contributing

> ⚠️ This card is **work in progress and untested** — see the [README](README.md).

## Branch policy

`main` is protected and **cannot be pushed to directly** — every change goes through a pull
request:

1. Create a branch and commit your change there.
2. Open a pull request against `main`.
3. CI must pass: **Prettier** (syntax + formatting) and **HACS** (plugin validation).
4. Merge once all checks are green.

Force-pushing to and deleting `main` are disabled for everyone.

## Development

```bash
node --check clawdmeter.js
npx prettier --check "**/*.js"   # or: npx prettier --write "**/*.js"
```

The custom element is `clawdmeter-card`. The file must stay named `clawdmeter.js` so HACS
(repo `lovelace-clawdmeter`) can find it.
