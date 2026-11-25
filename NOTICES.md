# Notices

**Cobblemon** is by the Cobblemon Contributors (cable-mc): <https://cobblemon.com>, source
<https://gitlab.com/cable-mc/cobblemon>. This is an **unofficial port** of Cobblemon to Minecraft 26.3 (Fabric),
versions `1.8.3+26.3-port.<n>`. It was **modified** from Cobblemon's source (branch `feature/version-bump-v2`, commit
c49a60a23a), and the changes are the port's commits on top of that. It is not made, endorsed or supported by the
Cobblemon team. Please report problems with it at <https://github.com/RhysSullivan/cobblemon-fabric-26.3/issues>,
not to them.

The source code of each release is attached to that release as `cobblemon-26.3-port.<n>-src.tar.gz`: a source
archive of the exact commit the jar was built from. The jar itself carries a short notice and every licence text
below (`cobblemon-port/` inside the jar).

| Part | Licence | Text |
|---|---|---|
| Cobblemon code, and the port's changes to it | Mozilla Public License 2.0 | `licenses/LICENSE-Cobblemon-MPL-2.0.txt` |
| Cobblemon assets: models, animations, textures, sounds, lang files and the built-in resource packs | Creative Commons Attribution-NonCommercial 3.0 Unported, as stated in the `license` file in each model folder of Cobblemon's source (also in the jar) | `licenses/LICENSE-Cobblemon-assets-CC-BY-NC-3.0.txt`. **Non-commercial use only.** |
| Pokémon Showdown battle engine (`data/cobblemon/showdown.zip`), Guangcong Luo and contributors | MIT | `licenses/LICENSE-showdown-MIT.txt` |

**Changes the port made to Cobblemon's assets.** Every other asset is unmodified:
- `assets/cobblemon/shaders/core/particle_base.vsh`, `particle_add.fsh`, `particle_cutout.fsh`: rewritten in the
  shader dialect Minecraft 26.3 requires; the effect is unchanged.
- `assets/cobblemon/lang/en_us.json`: two entries added for the port.
- From port.4: `data/cobblemon/structure/habitats/sunflowerbed_clearing5.nbt` and `parched_peat_bog7.nbt`: one
  misspelt jigsaw block state each corrected (`minecraft:dirt_block` to `minecraft:dirt`, `minecraft:strucutre_void`
  to `minecraft:structure_void`).
- From port.4: `data/cobblemon/loot_table/shipwreck_coves/fishing_boats/fishing_boat.json`: the treasure map's item
  is `minecraft:filled_map` instead of `minecraft:map` (Minecraft 26.3's `exploration_map` function fills in the item
  it is given; on 1.21.1 it replaced it).

Nested in the jar (`META-INF/jars/`, unmodified; licences read from each artifact's published POM):

| Nested jar | Licence | Text |
|---|---|---|
| `molang-1.1.20.jar` (Cobblemon's MoLang fork) | GPL-3.0 | `licenses/LICENSE-MoLang-GPL-3.0.txt`. **Corresponding source:** gitlab.com/cable-mc/molang at afbcf03a (version 1.1.20, the same classes as the jar), attached to each release as `molang-afbcf03a.tar.gz` |
| `polyglot`, `graal-sdk`, `collections`, `word`, `nativeimage`, `jniutils` 25.0.2 (Oracle GraalVM SDK) | Universal Permissive License 1.0 | `licenses/LICENSE-GraalVM-sdk-UPL-1.0.txt` |
| `truffle-api` 25.0.2 | UPL 1.0 | `licenses/LICENSE-GraalVM-truffle-UPL-1.0.txt` |
| `regex` 25.0.2 | UPL 1.0 | `licenses/LICENSE-GraalVM-regex-UPL-1.0.txt` |
| `js-language` 25.0.2 (GraalJS) | UPL 1.0, and MIT for third-party code it includes | `licenses/LICENSE-GraalJS-UPL-1.0.txt`, `licenses/THIRD_PARTY-GraalJS.txt` |
| `xz` 25.0.2 (GraalVM's repackaged XZ for Java) | UPL 1.0 | `licenses/LICENSE-GraalVM-sdk-UPL-1.0.txt` |
| `icu4j` 25.0.2 (GraalVM's repackaged ICU4J) and `icu4j` 71.1 | Unicode/ICU License | `licenses/LICENSE-ICU-Unicode.txt` |
| `mongodb-driver-core`, `mongodb-driver-sync` 4.10.2 | Apache 2.0 | `licenses/LICENSE-Apache-2.0.txt` |

The jar needs **Fabric Language Kotlin** 1.14.2 (FabricMC, Apache 2.0) installed beside it. It is not inside the
jar.

Pokémon names, designs and Pokédex texts are trademarks and copyright of Nintendo, Creatures Inc. and GAME FREAK inc.
Cobblemon is a non-commercial fan project, and this port is free and non-commercial.
