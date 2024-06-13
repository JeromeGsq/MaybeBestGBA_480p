# `MaybeBestGBA_480p` shader (according to me)

<img src="./screenshots/shader.png"/>

# Download `MaybeBestGBA_480p` : [Link to zip file](https://github.com/JeromeGsq/MaybeBestGBA_480p/archive/refs/heads/MaybeBestGBA_480p.zip)

# `MaybeBestGBA_480p` shader configuration for RetroArch on Anbernic RG35XX

This guide will help you install and configure shaders, overlays and filters for MaybeBestGBA_480p for RetroArch on Anbernic RG35XX devices (plus, H and SP). The old is not 

This shader may not be the most faithful, so you'll have to adjust it yourself to suit your needs.
At a typical eye distance, I find it tries to be the sharpest and the most aligned with the resolution.
These are my personal tastes.

If you use another device, go to here: [Link](#other).

See screenshots here: [Link to screenshots](./SCREENSHOTS.md).

## Prerequisites

- An Anbernic RG35XX (old, plus, H or SP) or other device with 640x480 resolution.
- Retroarch installed.
- A computer with a microSD card reader or FTP connection.
- The zip file containing the 'retroarch' folder.

## Step 1: Download link

1. **Download the necessary files:**
   - `MaybeBestGBA_480p` : [Link to zip file](https://github.com/JeromeGsq/MaybeBestGBA_480p/archive/refs/heads/MaybeBestGBA_480p.zip)

2. **Unzip the file:**
   - Unzip the file and copy/overwrite the `/retroarch` folder on your SD card.

> ❓ Wat daz it do: 
>
> It will copy these files into this folder structure.
>
> It may ask to overwrite some files (`Normal2x.filt` & `normal2x.so` for example, click `no`).
> ```sh
> retroarch/
> ├── filters/
> │   └── video/
> │       ├── Normal2x.filt
> │       └── normal2x.so
> ├── overlays/
> │   └── _maybe_best_gba_480p/
> │       └── Perfect_GBA_for_RG35XX/
> │           ├── Perfect_GBA_RG35XX.cfg
> │           ├── Perfect_GBA_RG35XX.png
> │           └── ...
> └── shaders/
>     └── _maybe_best_gba_480p/
>         ├── _maybe_best_gba_480p.glsl
>         ├── fast-sharpen.glsl
>         ├── image-adjustment.glsl
>         └── sharp-shimmerless.glsl
> ```

##  Step 2: Configure your device
   >For the next part, here is a legend:
   >
   > ⚪️: set to `OFF` or `default value`
   >
   > 🟢: set to `ON`
   >
   > 🔵: use custom setting

1. **Launch a GBA game from retroarch**
   - For example `Pokemon` or `MegaMan` where you can find text.

2. **Settings -> Video -> Output**

```
🔵 Video : gl
...
```

3. **Settings -> Video -> Scaling:**

```
⚪️ Integer Scale: off 
⚪️ Integer Scale Overscale: off 
🔵 Aspect Ratio: Custom
🔵 Custom Aspect Ratio (X Position): -1
🔵 Custom Aspect Ratio (Y Position): 0
🔵 Custom Aspect Ratio (Width): 642
🔵 Custom Aspect Ratio (Height): 424
🟢 Bilinear Filtering: on
⚪️ Crop Overscan (Restart required): off
```

4. **Settings -> Video**

```
...
🔵 Video filter: Normal2x
...
```

5. **Quick Menu -> On-Screen Overlay**

```
🟢 Display Overlay: on
🔵 Overlay Preset: ./overlays/_maybe_best_gba_480p/Perfect_GBA_for_RG35XX/Perfect_GBA_RG35XX.cfg
🔵 Overlay Opacity: 0.5
...
```

6. **Quick Menu -> Shaders**

```
🟢 Video Shaders: on
...
```
- Select `Load Preset` and set it to `./shaders/_maybe_best_gba_480p/_maybe_best_gba_480p.glsp`.

- **If you want**, select `Shader Parameters` to tweak values. You may change these settings as your taste:
```
🔵 Target Gamma: -
...
🔵 Saturation: -
...
🔵 Red Channel: -
🔵 Green Channel: -
🔵 Blue Channel: -
...
...
...
🔵 Sharpen strenght: -
🔵 Ammount of sharpening: Don't go to high, limit the value between 0.7 and 0.15
🔵 Details sharpened: -
```

7. **Save your changes**
- in `Quick Menu -> Shaders`, select `Save Preset` and select `Save Core Preset`.
- in `Quick Menu -> Overrides`, select `Save Core Overrides` and select `Save Core Preset`.


## Bonus
1. **Add hotkey to switch shaders on/off**
- Go to `Settings -> Input -> Hotkeys`and set a key to `Shaders (Toggle)`.
- Now you can switch shaders on/off by pressing the hotkey to see the difference.

2. **Tweak the width and height of the screen to fix some uneven letters**
- Go to `Quick Menu -> On-Screen Overlay` and change the `Custom Aspect Ratio (Width)` between  638 and 642. 
- Go to `Quick Menu -> On-Screen Overlay` and change the `Custom Aspect Ratio (Hight)` between  424 and 428.
- This will help you to fix some uneven letters in the text, but it may not be perfect.

3. **Battery usage & heating & performances**
- If you notice that your device is heating up or the battery is draining too fast, you may want to disable the shaders and overlays when not in use.
- My RG35XX SP is a little bit warm, but it's not a problem for me. I don't know about the other devices.

## Other
- If you use another device, like Miyoo Mini Plus, use these overlays [1playerinsertcoin Overlays](https://www.reddit.com/r/MiyooMini/comments/18ovuld/i_made_a_game_boy_advance_overlay/).
- Configure `3. Settings -> Video -> Scaling:` to match your device resolution.


## Acknowledgements

Thanks to all the developers and contributors to the RetroArch and Anbernic community for their hard work and continued support.

- [RetroArch](https://www.retroarch.com/)   
- [Anbernic](https://www.anbernic.com/)
- [mugwomp93 Overlays](https://github.com/mugwomp93/GarlicOS_Customization/tree/main)
- [1playerinsertcoin Overlays](https://www.reddit.com/r/MiyooMini/comments/18ovuld/i_made_a_game_boy_advance_overlay/)
- [my mom](https://www.youtube.com/watch?v=dQw4w9WgXcQ)

---

**Note:** This guide is based on information available at the time of writing. Steps and links may change over time. Be sure to check official sources for updates and new versions.
