# Max Wolf's Homebrew tap

Homebrew formulae for tools by Max Wolf. Packages use prebuilt releases from
each project's official GitHub repository.

## Install

With [Homebrew](https://brew.sh/) installed, add this tap, trust the Commander
Wolf formula, and install it:

```sh
brew tap max-wolf-cpp/tap
brew trust --formula max-wolf-cpp/tap/cwolf
brew install max-wolf-cpp/tap/cwolf
```

The trust command authorizes only this formula. Homebrew 6 requires explicit
trust for third-party tap formulae.

Launch the file manager from a terminal:

```sh
cwolf
```

Commander Wolf requires an Apple Silicon Mac running macOS 14 (Sonoma) or newer.
Intel Macs and Linux are not supported by this formula. The complete release
includes Fox Media Term and its native runtime libraries; a separate FFmpeg
installation is not required. A Nerd Font is recommended for the default icons.
The binaries are ad-hoc signed and are not notarized.

## Packages

| Formula | Application | Platform | Command |
|---|---|---|---|
| [cwolf](Formula/cwolf.rb) | [Commander Wolf](https://github.com/max-wolf-cpp/commander-wolf) — a dual-pane terminal file manager with Vim-style controls, Lua configuration, and rich previews | macOS 14+, Apple Silicon | `cwolf` |

## Update

Refresh the taps and upgrade Commander Wolf:

```sh
brew update
brew upgrade max-wolf-cpp/tap/cwolf
```

## Uninstall

```sh
brew uninstall max-wolf-cpp/tap/cwolf
```

## Maintenance

The Commander Wolf formula is also maintained in
[`Packaging/Homebrew/`](https://github.com/max-wolf-cpp/commander-wolf/tree/master/Packaging/Homebrew)
in the application's repository. For a new release, update that source copy
with the versioned archive URL and the SHA256 from the published release's
`SHA256SUMS.txt`. Run **Validate Homebrew package** in that repository's GitHub
Actions, then synchronize the validated formula to this tap.

The workflow checks installation, original payload checksums, native library
loading and signatures, a short pseudoterminal session, removal, and repeated
installation on macOS ARM64. It does not validate real terminal graphics, media
playback, Gatekeeper behavior, or the macOS 14 minimum.

Formula updates must be committed and pushed here before users can receive them
through `brew update` and `brew upgrade`. When adding another tool, place its
formula in `Formula/` and add it to the package table above.

## License

The formulae and documentation in this repository are covered by the
[MIT license](LICENSE). Packaged applications and their dependencies retain
their respective licenses, included in each release archive.
