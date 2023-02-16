# Actions

A set of useful GitHub actions for Solana devs.

- [Install Rust](#install-rust)
- [Install Solana](#install-solana)

## Install Rust

Install Rust with components, verify the installed versions and set the rustc hash as a `RUSTC_HASH` environment variable.

```yaml
- uses: metaplex-foundation/actions/install-rust@v1
  with:
    toolchain: stable
    components: clippy,rustfmt
```

- Inputs:
  - `toolchain`: The Rust toolchain to install. Defaults to `stable`.
  - `components`: A comma-separated list of Rust components to install. Defaults to `clippy,rustfmt`.
- Outputs:
  - `cachekey`: The hash of the installed rustc.
  - `toolchain`: The name of the installed toolchain.

## Install Solana

Install Solana with optional caching and verify the installed version.

```yaml
- uses: metaplex-foundation/actions/install-solana@v1
  with:
    version: stable
    cache: true
```

- Inputs:
  - `version`: The Solana version to install. Defaults to `stable`.
  - `cache`: Whether the downloaded Solana release should be cached. Defaults to `true`.
