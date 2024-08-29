# Tooling

The Haskell tooling consists basically of the following:

| Tool            | Haskell                   | Rust            |
| --------------- | ------------------------- | --------------- |
| Installer       | `ghcup`                   | `rustup`        |
| Compiler        | `ghc`                     | `rustc`         |
| Package manager | `cabal`                   | `cargo`         |
| Language Server | `haskell-language-server` | `rust-analyzer` |

Use [GHCup][ghcup] to install the whole toolchain. You should figure it out pretty easily, it is quite similar to `rustup`
and works on Windows, MacOS and Linux.

If you are using Linux, avoid using your distribution's package manager, unless
you are using NixOS.

> **NOTE**: GHCup doesn't work on NixOS. Use the Nix package manager to install the toolchain. Refer to the
> [Haskell][nixos-wiki-haskell] page on NixOS Wiki for further information.

[ghcup]: https://www.haskell.org/ghcup/
[nixos-wiki-haskell]: https://nixos.wiki/wiki/Haskell
