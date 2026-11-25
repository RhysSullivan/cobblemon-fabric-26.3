# Cobblemon for Minecraft 26.3 Fabric (unofficial port)

An unofficial port of [Cobblemon](https://cobblemon.com) to Minecraft 26.3 on Fabric. **It is not made, endorsed
or supported by the Cobblemon team.** Please do not report problems with this port to them, on their tracker or
their Discord. Use [this repository's issues](https://github.com/RhysSullivan/cobblemon-fabric-26.3/issues)
instead.

Cobblemon is by the Cobblemon Contributors. The official mod is at <https://cobblemon.com> and on
[Modrinth](https://modrinth.com/mod/cobblemon), and its source is at <https://gitlab.com/cable-mc/cobblemon>. All
credit for Cobblemon goes to them. This port takes their source (branch `feature/version-bump-v2`, commit
c49a60a23a) and changes what Minecraft 26.3 needs. It is made for one free server and its pack.

## Download

Built jars are on the [releases page](https://github.com/RhysSullivan/cobblemon-fabric-26.3/releases). The jar's
version is `1.8.3+26.3-port.<n>`. It needs Fabric Loader 0.20.1 or later, Fabric API 0.166.2+26.3 or later,
Fabric Language Kotlin 1.14.2+kotlin.2.4.21 or later and Java 25. Client and server must use the same jar.

## Source

This repository holds only this README, the notices and the licence texts. The full source of each build is
attached to its release as `cobblemon-26.3-port.<n>-src.tar.gz`, an archive of exactly the commit the jar was
built from. That covers Cobblemon's tree and the port's changes, which are commits on top of it. Changed code is commented
`26.3 port` in most places. The source of the MoLang library nested in the jar is attached as well. To build:
`./gradlew :fabric:assemble` with Java 25. The game tests run with `./gradlew :fabric:runGameTest`.

## Licences

- Cobblemon's code and the port's changes to it: [Mozilla Public License 2.0](licenses/LICENSE-Cobblemon-MPL-2.0.txt).
- Cobblemon's assets (models, animations, textures, sounds and the rest under `assets/`):
  [Creative Commons Attribution-NonCommercial 3.0 Unported](licenses/LICENSE-Cobblemon-assets-CC-BY-NC-3.0.txt),
  by the Cobblemon Contributors. **Non-commercial use only.** The port changed three particle shaders, for the
  26.3 shader dialect, and added two English lang entries. Every other asset is unmodified.
- Everything else in the jar and its licence: [NOTICES.md](NOTICES.md). The jar carries the same notices and
  licence texts in `cobblemon-port/`.

Pokémon names and designs are trademarks and copyright of Nintendo, Creatures Inc. and GAME FREAK inc. Cobblemon is
a non-commercial fan project, and so is this port.
