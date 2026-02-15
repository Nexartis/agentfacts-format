# Nexartis Fork — agentfacts-format

This fork is maintained by [Nexartis](https://github.com/Nexartis) for [KnowYourModel](https://knowyourmodel.ai) (KYM) NANDA integration work.

## License

This project is licensed under the **MIT License** per the upstream project (Project NANDA). The upstream repo's `README.md` states "MIT License" but does not include a dedicated `LICENSE` file. All upstream copyright and license notices are preserved per MIT requirements.

## Upstream

| | |
|---|---|
| **Upstream repo** | [projnanda/agentfacts-format](https://github.com/projnanda/agentfacts-format) |
| **Fork date** | 2026-02-11 |
| **License** | MIT (declared in README) |

## About Nexartis

**[Nexartis](https://nexartis.com)** builds AI infrastructure for the agentic web:

- **[KnowYourModel](https://knowyourmodel.ai)** — The trust registry for AI agents and models. Decentralized identity (DIDs), W3C Verifiable Credentials, and NANDA global agent discovery.
- **[CubiCube](https://cubicube.app)** — Full-stack web application generation platform.
- **[Pegasus HB3](https://github.com/Nexartis/pegasus-hb3-engine)** — Horizon Breakthrough v3 build engine.

## Purpose

KYM uses the AgentFacts JSON schema as the canonical format for agent metadata served via `/api/agents/:id/facts`. This fork allows Nexartis to:
- Reference the schema for validating AgentFacts payloads
- Propose KYM-specific extensions (e.g. `trustScore`, `gitVerified`) for upstream review
- Track upstream schema evolution

## Branch Strategy

- `dev` — default branch (protected). All feature branches open PRs to `dev`.
- `prod` — production branch (protected). PRs from `dev` → `prod` after validation.
- Feature branches are created from `dev` for all work.

## Syncing with Upstream

```bash
# One-time setup (already done):
git remote add upstream https://github.com/projnanda/agentfacts-format.git

# Sync upstream changes into dev:
git checkout dev
git fetch upstream
git merge upstream/main
# Resolve any conflicts, then push:
git push origin dev
```

## Contributing Back Upstream

If you make changes that would benefit the upstream project:
1. Create a branch from upstream's `main`: `git checkout -b fix/my-change upstream/main`
2. Make your changes, commit, and push to origin
3. Open a PR on [projnanda/agentfacts-format](https://github.com/projnanda/agentfacts-format/pulls) from `Nexartis:fix/my-change`

## Nexartis-Specific Changes

| Date | Change | Files |
|---|---|---|
| 2026-02-11 | Initial fork + `NEXARTIS.md` added | `NEXARTIS.md` |
| 2026-02-15 | Updated NEXARTIS.md with fork best practices | `NEXARTIS.md` |

## Contact

- **GitHub:** [Nexartis](https://github.com/Nexartis)
- **Website:** [nexartis.com](https://nexartis.com)
