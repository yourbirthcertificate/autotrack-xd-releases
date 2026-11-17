# Auto Track XD: downloads

Auto Track XD turns a song file into a playable custom chart for Spin Rhythm XD: five difficulties, album art and synced lyrics, written straight into the game's `Custom` folder.

This repository holds the downloads only. Get them from [Releases](../../releases). There is no source code here.

## Which file

| File | What it is |
|---|---|
| `AutoTrackXD-<version>-setup.exe` | The installer. It installs for your user only and needs no administrator rights. |
| `AutoTrackXD-<version>-portable.zip` | The same app with no install. Unzip it anywhere; it keeps its data in a `data` folder beside the program. |
| `SHA256SUMS.txt` | Checksums for the two files above. |

The installed app checks this page for newer versions once a day and offers to update itself. Turn that off in Settings.

## Windows will warn you

The downloads are not code-signed, so Windows SmartScreen may say "Windows protected your PC". Choose **More info**, then **Run anyway**. To check that a file is the one that was published, compare its SHA-256 with `SHA256SUMS.txt`:

```powershell
Get-FileHash .\AutoTrackXD-<version>-setup.exe -Algorithm SHA256
```

## What it needs

- Windows 10 or 11.
- [ffmpeg](https://ffmpeg.org) on the path (`winget install Gyan.FFmpeg`).
- The first time you run it, it downloads an engine (Lite, about 0.4 GB, or Full, about 3 GB, for an NVIDIA graphics card) from pytorch.org and PyPI. You choose which.

## Privacy

Your audio never leaves your PC, except in the optional Cloud stems quality, which asks first. Looking up lyrics, categories and album art sends only text about the song (title, artist, album, length), and every lookup has a switch in Settings. There is no telemetry.

## Not affiliated

Auto Track XD is an independent fan tool. It is not affiliated with or endorsed by Super Spin Digital. Spin Rhythm XD is their game.
