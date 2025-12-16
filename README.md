
Resident Evil 3 / Biohazard 3 Classic Rebirth 3 HD Mod Loader allows "hires" texture assets and "zmovie" cutscenes/fmvs to load exclusively from the mod_hd folder. 

# 👑 RE3 Classic Rebirth 3: Self-Contained HD Mod Loader
This project provides a robust solution for loading the TeamX HD Mod assets (hires textures and zmovie cutscenes) exclusively from your dedicated mod folder, ensuring compatibility, stability, and control over your Resident Evil 3 experience.

# ✨ Key Features & Purpose
The core issue with previous modding setups was that the TeamX HD Mod loaded globally, often conflicting with Classic Rebirth 3's (CR3) mod switching feature. Furthermore "zmovie" only loaded from the root directory of the game. This solution fixes this:

* Self-Contained Assets: Loads hires texture folders, zmovie cutscene folders, and dump texture folders only from the mod_hd directory.

* Seamless Mod Switching: Allows users to easily switch between pure vanilla/original RE3/BIO3 and the full HD experience simply by choosing or excluding this mod.

* Texture Overrides & Dumping: Ensures that any custom low-resolution textures already present in your mod are used first, and the HD Mod's dumping feature works correctly, placing upscaling-ready files directly into your mod's local dump folder.

* Full MP4 Movie Support: Leverages CR3's built-in MP4/MPEG loading functionality to load any correctly named MP4 movies from the mod_hd/zmovie/ path. Movies no longer have to be always be HD nor globally affecting all mods if you don't want them to be.

# 💾 Requirements
To use this mod, you must have the following base files and environment set up:

* Game Version: Biohazard 3 Sourcenext / [Resident Evil 3 GOG](https://www.gog.com/en/game/resident_evil_3) version.

  * Region (GOG): Must be set to Japan region for it to be compatible with Classic Rebirth 3.

* Patches:

  * [Sourcenext 1.1.0 Patch](https://classicrebirth.com/index.php/download/biohazard-3-sourcenext-1-1-0-patch/).
  * [Classic Rebirth 3](https://classicrebirth.com/index.php/download/resident-evil-3-classic-rebirth/) (place ddraw.dll in your game root next to BIOHAZARD(R) 3 PC.exe).

* HD Mod Files: You must provide the following files and folders from the TeamX HD Mod / [Seamless HD Mod](https://www.reshdp.com/re3/):

  * dinput8.dll (file) - currently included

  * libwebp.dll (file) - currently included

  * bio3hd.asi (file) - currently included

  * hires (folder)

 * Extra
   * [HD Movies](https://classicrebirth.com/index.php/download/re3-hq-movies/) (By Darren) 
   * [HD Voices](https://www.moddb.com/addons/resident-evil-3-high-quality-voices-pack) (By Reza Molaee; Merci Azizam)
   * [OST/MUSIC Overhaul](https://www.moddb.com/addons/resident-evil-3-nemesis-ost-overhaul-addon-sourcenext) (By Saigen and Cavatina) - I love this one!

# 📦 Installation Instructions
Meet all Requirements: Ensure your game is properly patched with CR3 (ddraw.dll).

* In the root directory of your game, put the folder named "mod_hd" there.

* Place HD Mod Files: Place dinput8.dll, libwebp.dll, and bio3hd.asi directly inside the mod_hd folder. These (besides "hires" folder) are included for the time being but in case they get updated, replace them as such.

* Place Assets: Place the downloaded HD assets (hires; for HD texture, zmovie; for HD movies, DATA_A; for HD Audio mod, etc.) inside the mod_hd folder. The folder "hires" and dinput8.dll, libwebp.dll, and bio3hd.asi usually come packed with TeamX HD mod or Seamless HD mod.

* Your directory should look like the following image

<img width="683" height="426" alt="image" src="https://github.com/user-attachments/assets/855a8c79-0633-4323-8117-4827317bdca9" />

* Launch the Mod: When you boot up BIOHAZARD(R) 3 PC.exe, select Resident Evil 3 - HD and walla!

# 🖼️ Texture Workflow Example
If you have a custom low-resolution Jill mod installed, the texture workflow is managed entirely within the mod_hd directory:

The game uses your custom low-res texture (e.g., DATA/PLD/PL00.PLD).

The HD Mod intercepts the textures and dumps them to: mod_hd/dump/.

You can upscale that WEBP file to 4x resolution.

You place the new high-resolution file in the matching location. E.G. if it was "mod_hd/dump/bgd/XXXXXX.webp" then the updated/modded/upscaled version goes in "mod_hd/hires/bgd/" in other words, the full path would become "mod_hd/hires/bgd/XXXXXX.webp".

# Custom DLL / Future Updates

A source code will be provided for those who would like to create a custom mod dll for use with their own mods, to load hires textures for said mod, all you would need to do is change mod_hd lines (few ones in hacks.cpp) and build! Then copy the provided dll in project_dir/Debug and use it with your mod_folder, just make sure the module section of your manifest.txt (in your mod_folder) refers to said dll.

Future update: There is also the possibility to make it work with just about any mod_folder, like mod_nemesis or mod_lon.

This is useful for users who not only want to use hires textures with their mods, but also add custom game-code changing functionalities to their game alongside the HD Texture/Movie loader functionality.
