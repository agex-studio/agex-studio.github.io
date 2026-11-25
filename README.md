# agex-studio.github.io

A copy of [agex-studio-apps](https://github.com/ashenfad/agex-studio-apps),
the sandbox page agex.studio runs agent-made apps in, served at
`https://agex-studio.github.io` for test_app's hidden test frames.

That origin is at another site than agex.studio, so the browser gives a
test frame a process of its own. Memory the test leaves behind goes away
with that process, and a slow screenshot doesn't freeze the studio's
tab. The live app preview stays on `apps.agex.studio`.

Nothing is edited here. `.github/workflows/deploy.yml` copies
agex-studio-apps' `main` (without its `CNAME` and `auth-relay.html`)
and publishes it, when agex-studio-apps sends a `repository_dispatch`,
once a day, or on demand:

```bash
gh workflow run deploy.yml -R agex-studio/agex-studio.github.io
```
