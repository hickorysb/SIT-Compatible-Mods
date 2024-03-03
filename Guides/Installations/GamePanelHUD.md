Files you need:
- Game Panel HUD v2.7.8: https://hub.sp-tarkov.com/files/download/8038/
- GPHUD-SIT-PATCH.zip: https://github.com/hickorysb/Game-Panel-HUD-SIT-Patcher/releases/download/v1.0.2/GPHUD-SIT-PATCH.zip

Steps to update:
- Delete any existing `EFTApi` and Game Panel HUD files
- Proceed to patch as if it's a new install

Steps to patch a new install:
1. Install Game Panel HUD into the BepInEx plugin folder like normal
3. Extract or copy the contents of `GPHUD-SIT-PATCH.zip` into the BepInEx plugins folder
4. Locate the `apply patch.bat` file copied into your plugins folder and double click to run it
5. Once the patch completes, GPHUD has been patched as long as you do not see any errors in any of the output
6. You may now delete the `Patches` folder, the `xdelta3.exe` file, and the `apply patch.bat` file