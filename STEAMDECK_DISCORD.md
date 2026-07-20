**Bloobs mods on Steam Deck / Linux**

Should work fine, it all runs through Proton. Heads up I haven't tested this on a Deck myself, so lmk if anything's off.

**Setup:**
1. Force Proton on the game: right-click **Bloobs Adventure Idle → Properties → Compatibility → Force the use of a specific Steam Play compatibility tool** (Proton Experimental or a recent stable).
2. Grab the all-in-one zip and extract it into the game folder (right-click game → Manage → Browse local files) so `winhttp.dll` and the `BepInEx` folder sit next to `Bloobs Adventure Idle.exe`. Same as the Windows install.
3. Launch the game once, then close it. This lets everything generate its folders.
4. Right-click **Bloobs → Properties → General → Launch Options** and paste this in:
```
WINEDLLOVERRIDES="winhttp=n,b" %command%
```
That line is the whole trick, it tells Proton to load the mod loader. Without it the mods just won't show up.
5. Launch again. Press **F1** in-game for the mod settings menu.

Use the normal **Windows** pack, not a Linux BepInEx build, the game's the Windows exe running under Proton.

If F1 does nothing on the Deck, plug in a keyboard or map a key to a controller button in Steam Input.
