# SDD Template

This is a project starter that calls reusable workflows from `sdd-foundation` and ships the minimal structure,
scripts, prompts, and niceties to start Spec-Driven Development in Windsurf.

## Quickstart
```
bin/new-feature "My First Feature"
# edit specs/NNN-*/feature-spec.md (add Examples + [NEEDS CLARIFICATION])
bin/generate-plan
# run tests (they should fail), commit, open PR
```

---
## Keep it simple, secure, efficient, token-aware
- **Simple**: start with `bin/new-feature` → `bin/generate-plan`. Open a PR; CI runs automatically.
- **Secure**: put API auth in **Settings → Secrets → Actions → `SCHEMA_AUTH_HEADER`** (e.g., `Authorization=Bearer ...`).
- **Efficient**: run `scripts/publish-metrics.sh` locally to generate tiny JSON artifacts for CI.
- **Token-aware**: paste only failing tests + target snippet to agents; rely on MCP tools where available.
