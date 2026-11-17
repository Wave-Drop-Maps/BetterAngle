# BetterAngle Pro

An open-source overlay for Windows that shows your exact compass angle in Fortnite, to the decimal.

BetterAngle reads your mouse movement straight from the hardware and turns it into degrees using your
in-game sensitivity. It never reads or changes the game's memory or files.

## Download

Get the latest installer, `BetterAngle_Setup.exe`, from the
**[Releases](https://github.com/Wave-Drop-Maps/BetterAngle/releases/latest)** page.
Once installed, the app keeps itself up to date.

## How to use

1. Enter your Fortnite sensitivity.
2. In a match, press the **Select ROI** key and drag a box around the on-screen text BetterAngle should watch
   (leave a little extra room). Then pick the colour to track (the white of the text).
3. Adjust **Percent** to how much of that area the text fills.

## Features

- **Raw input tracking**: mouse movement is read directly from the hardware.
- **Dive and glide detection**: fast pixel scanning of the area you chose tells skydiving from gliding,
  so the right turn speed is used.
- **Transition modes**: choose how dive/glide changes are handled: *Block input* (exact angle) or
  *Blend* (never touches your input). See [docs/INPUT_LOCK.md](docs/INPUT_LOCK.md).
- **Transparent overlay**: click-through and always on top, so it stays out of your way.
- **Automatic updates**: new releases install themselves.
- **Light on resources**: under 60 MB of memory and around 0.5% CPU.

## Fair play

- BetterAngle does not read or change game memory or files.
- Do not use it in competitive matches or tournaments.
- You use it at your own risk. The authors are not responsible for any account action.

## Building from source

Requirements: Visual Studio 2022 or later (MSVC), CMake, Ninja and Qt 6.5.3 (`win64_msvc2019_64`).

```
git clone https://github.com/Wave-Drop-Maps/BetterAngle.git
cd BetterAngle
cmake -B build -G Ninja -DCMAKE_BUILD_TYPE=Release
cmake --build build
```

Run these from a *Developer PowerShell for Visual Studio* so MSVC is on the path. Official releases are built by
GitHub Actions; see [CONTRIBUTING.md](CONTRIBUTING.md).

## License

Free for personal, educational and non-commercial use. See [LICENSE](LICENSE).

---

Made by [Fruss](https://github.com/wavedropmaps), [MahanYTT](https://github.com/MahanYTT) and
[itsdolphin](https://github.com/byu163) for [Wave Drop Maps](https://github.com/Wave-Drop-Maps).
