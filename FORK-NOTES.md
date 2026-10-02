# Personal fork notes

This fork (starxjys/fabulously-optimized) carries personal changes on top of upstream
Fabulously Optimized. They are documented here instead of in
[INCLUDED-MODS.md](INCLUDED-MODS.md), because upstream rewrites that table every release
and a personal section there breaks the daily upstream sync
(.github/workflows/sync-upstream.yml).

## Personal fork changes (MC 26.2 / custom-26.2 branch)

- Removed: [Cape Provider](https://www.curseforge.com/minecraft/mc-mods/cape-provider) (kept in older FO versions as listed above)
- Added: [CustomSkinLoader](https://modrinth.com/mod/customskinloader) (15.0.1-Universal) - skin & cape loading
- Added: [Voxy](https://modrinth.com/mod/voxy) (0.2.18-beta) - unlimited render distance (LODs; shaders need explicit voxy support)
- Added: [Xaero's Minimap](https://modrinth.com/mod/xaeros-minimap) (fabric-26.2-26.4.2) - minimap
- Added: [Xaero's World Map](https://modrinth.com/mod/xaeros-world-map) (fabric-26.2-1.44.2) - full-screen world map
- Added: [OneKeyMiner](https://modrinth.com/mod/onekeyminer_nf) (26.2-1.6.9-fabric) - hold-to-chain mining & farming

## Personal fork changes (MC 26.2 / rso-26.2 branch)

Same as custom-26.2, except:
- Removed: [Xaero's Minimap](https://modrinth.com/mod/xaeros-minimap), [Xaero's World Map](https://modrinth.com/mod/xaeros-world-map) (replaced by JourneyMap)
- Added: [JourneyMap](https://modrinth.com/mod/journeymap) (26.2-6.0.5+fabric) - minimap / fullscreen map / web map

RSO (红石生电优化) technical mod set added on top:
- Redstone/technical: MaLiLib, Litematica, Axiom, Flashback, Carpet, Tweakeroo, MiniHUD, ItemScroller, Litematica Printer, Servux, Pistorder
- QoL: AppleSkin, Jade, Inventory Profiles Next, Clumps, Bobby, Dynamic Crosshair, Better Statistics Screen, Sounds, Resourcify, Blur+, Punchy!, ItemSwapper, Peek, Chest Tracker (unofficial port), DawnGuiReader
- UI: FancyMenu, Controlling
- Auto-added deps: libIPN, Searchables, Konkrete, Melody, TCDCommons API, MRU
- Not included (no required dependents): Collective, Balm, GeckoLib, MidnightLib
- Controlify: re-enabled 2026-10-02 with Controlify 3.5.3+mc26.2 (it was kept as `controlify-3.4.1+mc26.2-universal.jar.disabled` since 2026-08-20). The startup crash came from ItemSwapper 1.0.0-beta.2 declaring a `controlify` entrypoint class that was missing from its jar; ItemSwapper 1.0.0-beta.3-26.2 ("Fix controlify in 26.1+") fixes that, so ItemSwapper and Controlify now run together.
