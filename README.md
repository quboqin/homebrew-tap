# Multica Homebrew tap

Homebrew distribution for the CLI from [quboqin/multica](https://github.com/quboqin/multica).

## Availability

This tap is initialized for automated releases. `Formula/multica.rb` will be
created by the first successful CLI/Homebrew publish in the source repository's
Release workflow. Until that formula exists, the installation command below is
not available.

This tap packages the command-line client. Desktop installers are published as
[GitHub Release assets](https://github.com/quboqin/multica/releases).

## Install and update

After the first formula is published:

```sh
brew tap quboqin/tap
brew install quboqin/tap/multica
multica version
```

To update:

```sh
brew update
brew upgrade quboqin/tap/multica
```

Use the fully qualified formula name to select this distribution. If an existing
Multica installation owns the same executable, resolve that installation before
linking this formula; do not overwrite it blindly.

If your Homebrew version asks you to trust this third-party formula, review the
formula and follow Homebrew's trust prompt. See [Tap Trust](https://docs.brew.sh/Tap-Trust).

## Release maintenance

- Source releases come from reviewed commits on `quboqin/multica`'s `qqb_main` branch.
- This tap's default and publishing branch is `main`.
- GoReleaser maintains `Formula/multica.rb` using the source repository's
  `HOMEBREW_TAP_GITHUB_TOKEN` Actions secret.
- The token should select only `quboqin/homebrew-tap`, with Contents read/write
  and the required Metadata read permission. Renew the token before its expiry
  and replace the secret in the source repository.
- The publisher writes directly to `main`; do not require pull requests or
  restrict branch updates unless the publishing workflow is changed accordingly.
- Do not manually invent release URLs or checksums. The formula is generated
  from the actual release archives and their checksums.

See the source repository's [release runbook](https://github.com/quboqin/multica/blob/qqb_main/.github/RELEASING.md).

## License

The packaged application is distributed under the source repository's
[Multica License](https://github.com/quboqin/multica/blob/qqb_main/LICENSE).
