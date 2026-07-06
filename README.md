# Gald3r Agent

> # ⚠️ EXPERIMENTAL BUILD — EXPECT FLAWS
> **Gald3r Agent is pre-1.0, experimental software built by a solo developer.**
> Expect bugs, rough edges, missing features, and breaking changes between releases.
> **Do not rely on it for anything critical.** Binaries carry a minisign integrity
> signature (verified automatically on install) but are **not yet OS-code-signed**,
> so Windows SmartScreen / macOS Gatekeeper will still warn.
> Use at your own risk — and please [report what breaks](#reporting-issues).

Command-line agent for the gald3r ecosystem.

**Current release: [v0.2.0](https://github.com/Gald3r-Labs/gald3r_agent/releases/latest)**

## Download

Get the latest binary from the [**Releases page**](https://github.com/Gald3r-Labs/gald3r_agent/releases).

| OS | File | First-launch note |
|----|------|-------------------|
| Windows | `gald3r-windows-x86_64.exe` (or `.msi`) | SmartScreen may say "unknown publisher" → **More info → Run anyway** |
| Linux | `gald3r-linux-x86_64` | `chmod +x` then run |
| macOS (Apple Silicon) | `gald3r-macos-arm64` | Gatekeeper says "unidentified developer" → **right-click → Open** (unsigned until Apple enrollment) |

> The OS warnings above come from the binaries not being **OS-code-signed** yet (no Windows
> Authenticode / Apple notarization). They are expected and safe to bypass. Code-signing and
> notarization will remove them in a future release.

## Verify your download

Every binary asset ships two sidecars:

- **`<asset>.sha256`** — SHA-256 checksum (integrity).
- **`<asset>.sig`** — minisign signature (authenticity), signed with the gald3r release key
  `F110B9BD6FF00BA2`.

`gald3r install agent` verifies both automatically — locally and offline — before installing or
upgrading. To check manually with [minisign](https://jedisct1.github.io/minisign/):

```
minisign -Vm gald3r-linux-x86_64 -P RWSiC/BvvbkQ8b7JpjwjDG4YUbyjBECa/t9EX/CKRe15yBuIQpV81rwA
```

## Reporting Issues

Found a bug or have a request? Please open an issue — this is how a solo dev finds out what's broken:

- **Bugs / problems:** [Open an issue](https://github.com/Gald3r-Labs/gald3r_agent/issues/new/choose) on this repo.
  Include your OS, the release version, and what you did / expected / saw.
- **Security vulnerabilities:** **Do not** open a public issue. Email the maintainer directly.

## Contributing

Gald3r Agent is built and maintained by a **solo developer** and is distributed as
**compiled binaries only — it is not open source** (the application source is private).

**Direct code contributions (pull requests) are not accepted at this time.** However, you are
warmly encouraged to:

- **Report bugs** and **request features** via [Issues](https://github.com/Gald3r-Labs/gald3r_agent/issues) — they are read and often adopted.
- Build plugins / extensions that interoperate with gald3r (the license permits this).

All accepted ideas are implemented by the maintainer and credited in the release notes.

## About this repository

This is a **downloads-only** repository: it hosts published binaries and nothing else.
Gald3r Agent is built from a **private** monorepo — the application source code is **not**
public and is not distributed here. gald3r is built *with* gald3r.

## License

Gald3r Agent is **proprietary — all rights reserved** (© 2025-2026 Gald3r Labs LLC).

See [LICENSE](LICENSE) for the copyright notice and [EULA.md](EULA.md) for the
End User License Agreement governing use of the binary: a license to **use** it
only — **no redistribution, no reverse-engineering, no warranty** (experimental phase).
