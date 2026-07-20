# Bloobs Adventure Idle — All-in-One Mod Pack

Everything you need to mod **Bloobs Adventure Idle**, in a single download. The mod loader, the
in-game settings menu, and all four mods — pre-bundled so you don't have to piece it together.

## What's inside

| Component | Version | What it does |
|-----------|---------|--------------|
| [BepInEx](https://github.com/BepInEx/BepInEx) | 5.4.23.2 (x64) | The mod loader (third-party). |
| [ConfigurationManager](https://github.com/BepInEx/BepInEx.ConfigurationManager) | 19.0 | In-game settings menu — press **F1** (third-party). |
| [Auto Challenge Swap](https://github.com/Tanner3031/AutoChallengeSwap) | 2.16.0 | Auto-swaps your challenge tracker slots to match what you're doing. |
| [Challenge Navigator](https://github.com/Tanner3031/ChallengeNavigator) | 1.8.0 | Adds a **»** button to walk to an activity and start it. |
| [Craft Time Estimator](https://github.com/Tanner3031/CraftTimeEstimator) | 1.2.0 | Shows the time to craft the whole "Can make" amount under each recipe. |
| [Turbo Speed Control](https://github.com/Tanner3031/TurboSpeedControl) | 1.0.0 | Pick your turbo speed — 3x / 5x / 8x / 10x — from the menu. |

## Install

1. **Download** `BloobsMods-AllInOne.zip` from the [latest release](../../releases/latest).
2. Find your game folder — in Steam: right-click **Bloobs Adventure Idle → Manage → Browse local
   files**. You should see `Bloobs Adventure Idle.exe` there.
3. **Extract everything from the zip into that folder**, so that `winhttp.dll` and the `BepInEx`
   folder sit right next to the game's `.exe`. Merge/replace if prompted.
4. **Launch the game once.** BepInEx initializes and the mods go live.
5. Press **F1** in-game to open the settings menu and tweak any mod.

## Steam Deck / Linux

The mods work on Steam Deck and Linux. Bloobs runs through **Proton**, so you use the exact same
Windows pack above, plus one launch option so Proton loads the mod loader.

1. Make sure Bloobs is set to run with **Proton** (Proton Experimental or a recent stable). In Steam:
   right-click **Bloobs Adventure Idle → Properties → Compatibility → Force the use of a specific
   Steam Play compatibility tool**.
2. Do the normal install above: extract the zip into the game folder so `winhttp.dll` and the
   `BepInEx` folder sit next to `Bloobs Adventure Idle.exe`.
3. **Launch the game once, then close it.** This lets Proton and BepInEx generate their folders.
4. In Steam, right-click **Bloobs Adventure Idle → Properties → General → Launch Options** and set:
   ```
   WINEDLLOVERRIDES="winhttp=n,b" %command%
   ```
   This is the one required step, it tells Proton's Wine to load BepInEx's `winhttp.dll` instead of
   the built-in stub. Without it the mods silently won't load.
5. Launch again. The mods go live and **F1** opens the settings menu as usual.

Notes:
- Use the **Windows x64** pack (this one), not a native Linux BepInEx build. The game itself is the
  Windows build running under Proton.
- If the settings menu doesn't respond to F1 on the Deck, map a keyboard key to a controller button
  in Steam Input, or plug in a keyboard, to press F1.

## Updating / removing

- Update one mod: drop its new `.dll` into `BepInEx\plugins\` (overwrite the old one). Each mod also
  has its own repo (linked above) with individual releases.
- Remove everything: delete `winhttp.dll`, `.doorstop_version`, `doorstop_config.ini`,
  `changelog.txt`, and the `BepInEx` folder from your game directory. The game runs vanilla again.

## Credits & licenses

BepInEx and ConfigurationManager are third-party tools, redistributed here **unmodified** under
their respective **LGPL** licenses — they are not my work. Full license texts are in the `licenses`
folder inside the zip. The four mods are **MIT**-licensed and made by
[Tanner3031](https://github.com/Tanner3031).

No files from Bloobs Adventure Idle itself are included or redistributed.
