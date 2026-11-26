# VpsInspect — namespace registry

Canonical list of **owned**, **reserved**, and **unclaimed** public identifiers for the `vpsinspect` project.
Last updated: **2026-11-26** (Phase 0).

Sibling organization: [`securemyvps`](https://github.com/securemyvps/.github/blob/main/NAMESPACES.md).

## GitHub

| Asset | Identifier | Status | Notes |
|---|---|---|---|
| GitHub org | [`vpsinspect`](https://github.com/vpsinspect) | **Owned** | Verified org |
| Primary repo | [`vpsinspect/vpsinspect`](https://github.com/vpsinspect/vpsinspect) | **Active** | Go module root, `main` protected |
| Org profile repo | [`vpsinspect/.github`](https://github.com/vpsinspect/.github) | **Active** | SECURITY.md, org profile, this file |
| Homebrew tap repo | [`vpsinspect/homebrew-tap`](https://github.com/vpsinspect/homebrew-tap) | **Reserved** | Public repo created 2026-11-26; no formulas until Phase 2 |
| Go module | `github.com/vpsinspect/vpsinspect` | **Claimed** | Tag `v0.0.1` claims the module proxy index |

## Distribution names

Checked 2026-11-26 by HTTP lookup. "Available" means the registry returned "not found" at that moment;
it is not a reservation — anyone can still claim it.

| Registry | Identifier | Status | Notes |
|---|---|---|---|
| Homebrew | `vpsinspect/tap/vpsinspect` | **Reserved** | Formula written in Phase 2+; install from `vpsinspect/homebrew-tap` |
| npm | `vpsinspect`, `@vpsinspect/cli` | **Available** | v1 is binary-only; register a private stub before Phase 2 |
| PyPI | `vpsinspect` | **Available** | Not used in v1 |
| RubyGems | `vpsinspect` | **Available** | Not used in v1 |
| crates.io | `vpsinspect` | **Available** | Not used (Go project) |
| Docker Hub | `vpsinspect/vpsinspect` | **Available** | No OCI image in v1 |
| GHCR | `ghcr.io/vpsinspect/vpsinspect` | **Available on first push** | Preferred if images ever ship; anonymous lookup returns 401 by design |

## Domains

| Asset | Identifier | Status | Notes |
|---|---|---|---|
| Domain | `vpsinspect.com` | **Owned** | DNSSEC / CAA / registrar transfer lock = Step 7 (manual) |

## Typosquat watchlist (do not use)

`vps-inspect`, `vpsinspect-cli`, `vpsinspector`, `vps-inspector`

## Maintainer actions

1. Before any npm publish: create the `vpsinspect` npm org and claim `vpsinspect` + `@vpsinspect/cli` with a **private stub** (no lifecycle scripts).
2. Step 7: enable DNSSEC + CAA + registrar transfer lock on `vpsinspect.com`.
3. Phase 2: add `Formula/vpsinspect.rb` to `vpsinspect/homebrew-tap` that pulls the signed `linux_amd64` / `linux_arm64` release assets and verifies `SHA256SUMS.txt`.
