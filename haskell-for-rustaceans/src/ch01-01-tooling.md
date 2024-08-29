# Tooling

The Haskell tooling consists basically of the following:

| Tool            | Haskell                   | Rust            |
| --------------- | ------------------------- | --------------- |
| Installer       | `ghcup`                   | `rustup`        |
| Compiler        | `ghc`                     | `rustc`         |
| Package manager | `cabal-install`           | `cargo`         |
| Language Server | `haskell-language-server` | `rust-analyzer` |

Use [GHCup][ghcup] to install the whole toolchain. You should figure it out pretty easily, it is quite similar to
`rustup` and works on Windows, MacOS and Linux.

If you are using Linux, avoid using your distribution's package manager, unless you are using NixOS.

> **NOTE**: GHCup doesn't work on NixOS. Use the Nix package manager to install the toolchain. Refer to the
> [Haskell][nixos-wiki-haskell] page on NixOS Wiki for further information.

## More about package managers

If you have seen some projects or browsed Haskell related content on the internet there is a chance that you might have
stumbled upon another Haskell package manger: `stack`. You might be wondering why did we chose `cabal-install` over
`stack`. The answer is simple: `cabal-install` is arguably simpler. It doesn't try to manage GHC or any other tooling
for you like `stack` does. There can be held a whole debate on to which one to choose. So we won't dwell on the topic.
The main thing you **need** no know is: both of them use the same library under the hood anyways. `cabal` is a library
that is used by both of the aforementioned package managers. We recommend using `cabal`.

Also, note that `cabal-install` provides the `cabal` executable. Hence, `cabal-install` is sometimes referred to as
`cabal` for the sake of simplicity. We'll consistently use `cabal-install` to refer to the package and `cabal` for the
library to avoid ambiguity. But be aware that in other sources or discussions, you might encounter `cabal` being used to
mean either the library or the executable.

[ghcup]: https://www.haskell.org/ghcup/
[nixos-wiki-haskell]: https://nixos.wiki/wiki/Haskell
