# Jesus' Intervention Just Arrived (JIJA) - Config Edition (Minecraft 26.3)

A client-side Fabric mod for Minecraft 26.3 that triggers a meme low-health visual overlay and church bells when your health drops to critical levels, now featuring a **complete in-game configuration screen integrated with Mod Menu**!

---

## Features

* **Mod Menu Integration:** Click on **Mods** -> **JIJA** -> **Configure** (or the gear icon) to open the in-game settings screen.
* **Configurable Health Threshold:** Slider from 0.5 to 10 hearts (1 to 20 HP). Default is 4 hearts (8 HP).
* **Sound Controls:** Toggle church bells ON/OFF and adjust sound volume from 0% to 100%.
* **Overlay Controls:** Toggle image overlay ON/OFF and adjust transparency/opacity (5% to 100%)
* **Repeat Delay:** Configure how frequently the warning flashes while health remains low (1.0s, 2.35s default, 3.5s, 5.0s).
* **▶ Test Effects Button:** Test audio and image overlay directly from the config screen without taking damage in-game.
* **Persistent Configuration:** Automatically saves and loads settings from `.minecraft/config/jija.json`.
* **Reset Defaults Button:** Restores vanilla JIJA settings

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
