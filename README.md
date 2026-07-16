# Flip Phone Launcher

A minimal, distraction-free Android launcher built for flip phones with a D-pad — like the CAT S22 Flip. Forked from [tanujnotes/Olauncher](https://github.com/tanujnotes/Olauncher).

## Why

Olauncher is a great minimal launcher, but it's designed for touchscreens. Flip phones like the CAT S22 have a touchscreen *and* a physical D-pad/keypad, and most launchers don't take advantage of that. This fork adds full D-pad navigation so the phone can be used one-handed, without touch, the way a flip phone is supposed to work.

## Features

- **D-pad app drawer navigation** — scroll through installed apps with the D-pad, no touch required
- **Long-press DOWN** on the home screen to open the app drawer
- **Long-press UP** on the home screen to open the notifications panel
- **Vertical app list** — icon on the left, app name on the right, fully navigable with up/down and select with the center key
- Built on top of Olauncher's minimal, clean home screen philosophy
- No conflicts with keypad dialing/T9 input

## Requirements

- Android device with a physical D-pad (tested on CAT S22 Flip)
- Some features (like opening the notification panel) may require the launcher to be installed as a system app, or granted the `STATUS_BAR` permission via ADB:
  ```
  adb shell pm grant fpLauncher android.permission.STATUS_BAR
  ```

## Building

APKs are built automatically via GitHub Actions on every push. Grab the latest build from the [Actions](../../actions) tab or [Releases](../../releases) page — no local build setup required.

If you'd rather build locally:

```
git clone https://github.com/ej360/flip-phone-launcher.git
cd flip-phone-launcher
./gradlew assembleDebug
```

Install via ADB:

```
adb install app/build/outputs/apk/debug/app-debug.apk
```

## Credits

Based on [Olauncher](https://github.com/tanujnotes/Olauncher) by [tanujnotes](https://github.com/tanujnotes). Huge thanks for the original minimal launcher foundation this project builds on.

## License

GNU General Public License (GPL), inherited from the original Olauncher project. See [LICENSE](LICENSE) for details.
