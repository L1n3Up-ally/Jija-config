# Jesus' Intervention Just Arrived (JIJA) - Config Edition (Minecraft 26.3)

A client-side Fabric mod for Minecraft 26.3 that triggers a meme low-health visual overlay and church bells when your health drops to critical levels, now featuring a **complete in-game configuration screen integrated with Mod Menu**!

---

## 🚀 Features

* **Mod Menu Integration:** Click on **Mods** -> **JIJA** -> **Configure** (or the gear icon) to open the in-game settings screen.
* **Configurable Health Threshold:** Slider from 0.5 to 10 hearts (1 to 20 HP). Default is 4 hearts (8 HP).
* **Sound Controls:** Toggle church bells ON/OFF and adjust sound volume from 0% to 100%.
* **Overlay Controls:** Toggle image overlay ON/OFF and adjust transparency/opacity (5% to 100%).
* **Image Selection:** Switch between:
  * `Random` (cycles between Jesus 1 and Jesus 2)
  * `Jesus 1`
  * `Jesus 2`
* **Repeat Delay:** Configure how frequently the warning flashes while health remains low (1.0s, 2.35s default, 3.5s, 5.0s).
* **▶ Test Effects Button:** Test audio and image overlay directly from the config screen without taking damage in-game.
* **Persistent Configuration:** Automatically saves and loads settings from `.minecraft/config/jija.json`.
* **Reset Defaults Button:** Restores vanilla JIJA settings anytime.

---

## 📦 Ready-to-Use Mod JAR

The compiled mod JAR is ready to install:
```
/home/sasha/jija-mod-26.3/build/libs/jija-1.0.9+mc26.3-config.jar
```

### Installation:
1. Copy `jija-1.0.9+mc26.3-config.jar` to your Minecraft `mods` folder (e.g. `~/.minecraft/mods/` or inside your Prism Launcher instance).
2. Ensure you have **Fabric Loader** (0.19.5+), **Fabric API** for 26.3, and **Mod Menu** (v21.0.0+ for 26.3) installed.
3. Launch Minecraft 26.3!

---

## 🛠 Project Structure

```
jija-mod-26.3/
├── build.sh                                    # Quick compilation script
├── build/libs/jija-1.0.9+mc26.3-config.jar    # Compiled mod JAR
└── src/main/
    ├── java/jesus/hp/
    │   ├── JIJA.java                          # Mod entrypoint & config initialization
    │   ├── SoundRegistry.java                 # Church bells sound registration
    │   ├── config/
    │   │   └── JijaConfig.java                # JSON config manager (load/save/defaults)
    │   └── client/
    │       ├── JIJAClient.java                # Client HUD registration
    │       ├── JesusHudOverlay.java           # HUD overlay rendering & audio trigger
    │       └── config/
    │           ├── JijaConfigScreen.java      # In-game Mod Menu configuration screen
    │           └── JijaModMenuApi.java        # Mod Menu API entrypoint
    └── resources/
        ├── fabric.mod.json                    # Fabric mod manifest with modmenu entrypoint
        └── assets/jija/                       # Textures, sounds, and icons
```

---

## ⚙ Config File (`config/jija.json`)

If you prefer editing the file directly, it is saved in `.minecraft/config/jija.json`:

```json
{
  "healthThreshold": 8.0,
  "soundEnabled": true,
  "soundVolume": 1.0,
  "soundPitch": 1.0,
  "overlayEnabled": true,
  "overlayMaxAlpha": 1.0,
  "imageMode": 0,
  "cycleDuration": 47.0,
  "fadeInDuration": 2.0,
  "fadeOutDuration": 20.0
}
```
