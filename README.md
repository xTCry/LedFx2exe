# Convert [`LedFx`] to exe

## Convert by [`auto-py-to-exe`]

1. Copy the [`XT.py`] file to the main [`LedFx`] folder and select it in __Script Location__

2. Icon: Select `LedFx/icons/favicon.ico`
3. Additiona Files: Add next folders
   * LedFx/ledfx_frontend => ledfx_frontend/
   * LedFx/ledfx/api => ledfx/api/
   * LedFx/ledfx/devices => ledfx/devices/
   * LedFx/ledfx/effects => ledfx/effects/
4. Advanced: 
   * In the __Output Directory__ field, set `LedFx/dist/`
   * In the __-n__ field, set `LedFx`
   * In the __--hidden-import__ field, set this:
```
ledfx.api.audio_devices,ledfx.api.config,ledfx.api.device,ledfx.api.device_effects,ledfx.api.devices,ledfx.api.effect,ledfx.api.effects,ledfx.api.info,ledfx.api.presets,ledfx.api.schema,ledfx.api.schema_types,ledfx.api.utils,ledfx.api.websocket,ledfx.devices.FXMatrix,ledfx.devices.e131,ledfx.devices.udp,ledfx.effects.audio,ledfx.effects.beat(Reactive),ledfx.effects.effectlets,ledfx.effects.energy(Reactive),ledfx.effects.fade,ledfx.effects.gradient,ledfx.effects.math,ledfx.effects.mel,ledfx.effects.modulate,ledfx.effects.pitchSpectrum(Reactive),ledfx.effects.rain(Reactive),ledfx.effects.rainbow,ledfx.effects.scroll(Reactive),ledfx.effects.singleColor,ledfx.effects.spectrum(Reactive),ledfx.effects.strobe,ledfx.effects.temporal,ledfx.effects.wavelength(Reactive)
```

5. Click to Convert button

### FIX
If you know how to make the **aubio** library not move to a separate folder, then you can skip this otherwise

Move this files from __dist__ to `aubio` folder

```sh
avcodec-58.dll
avformat-58.dll
avutil-56.dll
swresample-3.dll
```

6. Join to dist folder and run `LedFx.exe` file (:

<img src="https://raw.githubusercontent.com/xTCry/LedFx2exe/master/scrn1.jpg" alt="screenshot1" title="Example" height="90%">

[`LedFx`]: https://github.com/xTCry/LedFx
[`auto-py-to-exe`]: https://pypi.org/project/auto-py-to-exe/
[`XT.py`]: XT.py
