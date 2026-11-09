# Trails Flat

**The same game, cleaner.** Free mod that adds NVIDIA DLSS (DLAA) to Trails of Cold Steel on a normal screen, at your own resolution.

> **Cold Steel 1, 0.1.0 - pre-release.** Tested on one PC: Windows 11, RTX 4080 SUPER, 3440x1440, in field and battle. Save often.

**Quick start**

- Requires an NVIDIA RTX card, the PC game at version 1.6, and MSAA off in the game's launcher.
- Extract the ZIP and copy its three program files beside `ed8.exe`. If you use SenPatcher, rename its `DINPUT8.dll` first.
- Play as usual. F8 turns DLSS on or off.

[Releases](https://github.com/petonexus/trails-flat-releases/releases) - Looking for VR? See [Trails of Cold Steel VR](https://github.com/petonexus/tocs-vr-releases).

## What it does

- **Clean edges and a stable image.** DLSS runs inside the game, before bloom and the HUD, so menus and text are left alone.
- **Your resolution.** The 3D world renders at full size, so nothing is upscaled from a smaller picture.
- **Sharper textures.** 16x anisotropic filtering and a small sharpness bias on the 3D world.
- **Switch live.** Compare everything in-game with the keys below.
- **Safe failure.** If DLSS cannot run, the game keeps its normal picture and keeps running.

## Downloads

Download **trails-flat-cs1-0.1.0.zip** from the [latest release](https://github.com/petonexus/trails-flat-releases/releases).

SHA-256: `aea8fbb13c276ccd6c25eddd08c8417dc42cbed980d428d98e6862b55d061912`

**Verify a download.** Compare the SHA-256 of the ZIP (`Get-FileHash <zip>` in PowerShell) with the one on the release page.

## Requirements

- **Windows** 10 or 11, 64-bit.
- **GPU.** An NVIDIA RTX card with a current driver.
- **The game.** Trails of Cold Steel for PC, updated to version 1.6.
- **MSAA off** in the game's launcher. With MSAA on, DLSS stops by itself and you get the normal picture with no message.

## Install

The game folder is the one that holds `ed8.exe` (Steam: right-click the game > Manage > Browse local files). Back up any `DINPUT8.dll` you already have there.

**Without SenPatcher**

1. Copy `DINPUT8.dll`, `trails_flat_host.exe` and `nvngx_dlss.dll` into the game folder.

**With SenPatcher** (tested with v1.3.1)

1. In the game folder, rename SenPatcher's `DINPUT8.dll` to `DINPUT8_senpatcher.dll`.
2. Copy `DINPUT8.dll`, `trails_flat_host.exe` and `nvngx_dlss.dll` into the game folder.

If you run SenPatcher's "Patch Game" again, it replaces `DINPUT8.dll`. Repeat both steps, replacing the old `DINPUT8_senpatcher.dll`.

**The VR mod also uses `DINPUT8.dll`.** Do not install this over it, and do not rename the VR mod's DLL to `DINPUT8_senpatcher.dll`. If you also play in VR, use a separate copy of the game folder. Both still share the game's settings file, so the VR launcher can change the frame rate used here.

## Keys

| Key | Does |
| --- | --- |
| F8 | DLSS on or off |
| F9 | DLSS preset. Low beeps: 1 = K, 2 = M |
| F7 | Texture sharpness, with DLSS on. High beeps: 1 = normal, 2 = 16x anisotropic, 3 = 16x anisotropic and sharper |

Every launch starts with preset M and the sharpest textures. Preset M costs about 2.5 times as much as K, so on a slower RTX card press F9 for K. The game also receives these key presses.

## Known limits

- Only Trails of Cold Steel 1 is supported.
- Motion comes from the camera only, so fast-moving characters may leave a trail. None was seen in testing.
- Alt-tab, changing resolution, long cutscenes and long sessions have not been tested.
- The files are not signed, and a 64-bit helper runs hidden while the game runs. An antivirus may flag them.

If something goes wrong, the reason is in `trails_flat_hook.log` and `trails_flat_host.log` in the game folder.

## Uninstall

Delete `DINPUT8.dll`, `trails_flat_host.exe`, `nvngx_dlss.dll` and the two logs. If you use SenPatcher, rename `DINPUT8_senpatcher.dll` back to `DINPUT8.dll`.

## Optional

For sharper menus and HUD, [BigHead's HD Texture Pack](https://steamcommunity.com/app/538680/discussions/0/2579854400755735260/) works alongside this. It is a separate download and is not included.

## Licenses

Unofficial fan mod. No Falcom/NVIDIA endorsement. Trails IP belongs to its owners. Requires your own game; no game files. NVIDIA components have separate licenses.

The original mod portions are Copyright (c) 2026 petonexus; third-party components retain their own licenses. See [LICENSE.txt](cs1/LICENSE.txt) and [THIRD_PARTY_NOTICES.txt](cs1/THIRD_PARTY_NOTICES.txt).
