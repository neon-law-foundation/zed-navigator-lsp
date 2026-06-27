# Navigator LSP — Zed extension

**Navigator LSP** works for all Markdown documents, and we also enforce a superset of Markdown for notation templates.

Install it from Zed's extension store: open the command palette, run `zed: extensions`, search for **Navigator LSP**,
and click **Install**. On first run the extension downloads the matching `navigator-lsp` binary from the latest
[navigator GitHub Release](https://github.com/neon-law-foundation/navigator/releases) and caches it per version — there
is nothing else to install.

The prebuilt binaries today cover Apple Silicon macOS, x86-64 Linux, and x86-64 Windows. On any other platform, build
`navigator-lsp` yourself (`cargo install --path lsp` in the
[navigator](https://github.com/neon-law-foundation/navigator) repo) and put it on your `$PATH`, or set
`lsp.navigator-lsp.binary.path` in your Zed settings.

## This repository is generated

The extension source of truth lives in the navigator monorepo at
[`lsp/zed-ext/`](https://github.com/neon-law-foundation/navigator/tree/main/lsp/zed-ext). The navigator `deploy.yml`
syncs `src/lib.rs`, `Cargo.toml`, `Cargo.lock`, and `extension.toml` here on each release and pushes a `v<version>` tag;
this repo's [`release.yml`](.github/workflows/release.yml) then opens the version-bump PR to the
[`zed-industries/extensions`](https://github.com/zed-industries/extensions) registry. **Edit the extension in the
navigator repo, not here** — changes committed directly here are overwritten on the next release.

See [`docs/lsp/zed.md`](https://github.com/neon-law-foundation/navigator/blob/main/docs/lsp/zed.md) for the full
publishing pipeline and one-time setup.

## License

Dual-licensed under [Apache-2.0](LICENSE-APACHE) or [MIT](LICENSE-MIT), at your option.
