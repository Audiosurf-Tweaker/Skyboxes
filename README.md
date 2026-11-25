# Skyboxes

The `.sky` packages that ship with
[Audiosurf Tweaker](https://github.com/Unchpokable/Audiosurf-Tweaker). This repository is the source
the Tweaker's build copies into the game payload: everything tracked here is a package the player
gets.

## Contents

| | |
|---|---|
| `Canvas.sky/` | Submodule: [Canvas](https://github.com/Audiosurf-Tweaker/Canvas), the shipped sky. |
| `Nano Neon.sky/` | Submodule: [Nano-Neon](https://github.com/Audiosurf-Tweaker/Nano-Neon), an electronic neon sky in the spirit of Audiosurf 2 substratum. |
| `dev/` | Not tracked. Scratch packages and zipped copies while a package is being tested. |

A package is a folder whose name ends in `.sky`, with `Config.json` at its root. The zip form is the
same folder zipped and renamed to `<name>.sky`; the plugin loads both through the same path, and the
zip is what you ship.

## Why a submodule

Each sky is its own product with its own history, issues and release zip
(see [Canvas](https://github.com/Audiosurf-Tweaker/Canvas)). This repository only pins the versions
that ship, so one sky can be updated without rewriting the others. Cloning with
`--recurse-submodules` brings the packages in.

## Working on a sky

Edit the package in its own repository. To try a local edit in the game, drop the folder, or a zip
of it, into `Audiosurf\engine\TweakerStuff\SkyboxReplacer\Skyboxes\` and pick it in the Skybox tab
of the in-game overlay. `dev/` is ignored on purpose: it is where those scratch copies live.

The sky manual lives in the Tweaker's repository:
[Docs/skyboxes.md](https://github.com/Unchpokable/Audiosurf-Tweaker/blob/HEAD/Docs/skyboxes.md).

## Licence

MIT, see [LICENSE](LICENSE).
