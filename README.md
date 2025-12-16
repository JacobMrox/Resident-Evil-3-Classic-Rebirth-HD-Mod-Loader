# Resident-Evil-3-Biohazard-3-Classic-Rebirth-HD-Mod-Loader

RE3 Classic Rebirth 3 TeamX HD Mod Loader  This mod allows "hires" texture assets and "zmovie" cutscenes to load exclusively from the mod_hd folder. 

👑 RE3 Classic Rebirth 3: Self-Contained HD Mod Loader
This project provides a robust solution for loading the TeamX HD Mod assets (hires textures and zmovie cutscenes) exclusively from your dedicated mod folder, ensuring compatibility, stability, and control over your Resident Evil 3 experience.

✨ Key Features & Purpose
The core issue with previous modding setups was that the TeamX HD Mod loaded globally, often conflicting with Classic Rebirth 3's (CR3) mod switching feature. Your solution fixes this:

Self-Contained Assets: Loads hires texture folders, zmovie cutscene folders, and dump texture folders only from the mod_hd directory.

Seamless Mod Switching: Allows users to easily switch between pure vanilla/original RE3/BIO3 and the full HD experience simply by choosing or excluding this mod.

Texture Overrides & Dumping: Ensures that any custom low-resolution textures already present in your mod are used first, and the HD Mod's dumping feature works correctly, placing upscaling-ready files directly into your mod's local dump folder.

Full MP4 Movie Support: Leverages CR3's built-in functionality to correctly load any correctly named MP4 movies from the mod_hd/zmovie/ path.

💾 Requirements
To use this mod, you must have the following base files and environment set up:

Game Version: Biohazard 3 Sourcenext / Resident Evil 3 GOG version.

Region (GOG): Must be set to Japan region.

Patches: Sourcenext 1.1.0 Patch.

Base Loader: Classic Rebirth 3 (place ddraw.dll in your game root next to BIOHAZARD(R) 3 PC.exe).

HD Mod Files: You must provide the following files and folders from the TeamX HD Mod / Seamless HD Mod:

* dinput8.dll (file)

* libwebp.dll (file)

* bio3hd.asi (file)

* hires (folder)

📦 Installation Instructions
Meet all Requirements: Ensure your game is properly patched with CR3 (ddraw.dll).

Create Mod Folder: In the root directory of your game, create a folder named "mod_hd"

Place HD Mod Files: Place dinput8.dll, libwebp.dll, and bio3hd.asi directly inside the mod_hd folder.

Place Assets: Place the downloaded HD assets (hires, zmovie, dump, etc.) inside the mod_hd folder. These usually come packed with TeamX HD mod or Seamless HD mod.

Install Mod: Place the compiled hd.dll (the loader) and your manifest.txt file into the game mod direction root directory, alongside ddraw.dll.

🖼️ Texture Workflow Example
If you have a custom low-resolution Jill mod installed, the texture workflow is managed entirely within the mod_hd directory:

The game uses your custom low-res texture (e.g., DATA/PLD/PL00.PLD).

The HD Mod intercepts the textures and dumps them to: mod_hd/dump/.

You upscale that WEBP file to 4x resolution.

You place the new high-resolution file in the matching location. E.G. if it was "mod_hd/dump/bgd/XXXXXX.webp" then the updated/modded/upscaled version goes in "mod_hd/hires/bgd/" in other words, the full path would become "mod_hd/hires/bgd/XXXXXX.webp".
