
# Building Oasis for Windows

## Requirements

- Windows 10 or later
- Node.js 22.5 or later
- Git
- The complete Oasis client source and its required build assets

## Prepare the build dependencies

The build script requires these files and folders beside `app/`:

- `electron/`
- `electron-win/`
- `flash/`
- `tools/bin/rcedit-x64.exe`
- `installer/node_modules/`

These are not all included in the source ZIP. Obtain them using the project's original build setup before running the installer build.

## Install installer dependencies

Open a terminal in the client project folder and run:

```bash
cd installer
npm install
cd ..
```

## Build the Windows installer

Run the build script in a Bash environment that supports the project's requirements:

```bash
bash tools/build.sh windows
```

The default output is placed in `dist/`.

## Oasis installer name

The Windows installer output should be named:

`Oasis-Setup.exe`

The build script and installer configuration must agree on the output filename.

## Troubleshooting

If the build reports a missing file, check the required build assets above.
Do not rename the game executable until its launcher, installer, and protocol registrations have been updated together.
