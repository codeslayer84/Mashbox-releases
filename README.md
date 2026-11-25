# Mashbox

Mashbox is a small desktop app for researchers who need to change how a video looks before it is shown, shared or analysed. Open a 2D or 360° video, trim it, and give it a look: chalk, graphite, manga, oil daub, mosaic and others. Hide or protect parts of the picture with regions that follow the action. Cut a flat view out of a 360° video. Silence, bleep or disguise the voice in chosen stretches of the sound. Preview it live, then export.

It runs on macOS and Windows. This repository holds the downloads and nothing else; the source code is not published.

> **Status: early release (version 0.1.0).** [Fill in before publishing: which platforms are in this release and what has been tested.]

## What it does

- **Filters.** A chain of filters (Monochrome, Mosaic, Chalk, Poster, Manga, Cutout, Oil Daub, Flow Brush, Impasto, Wash, Graphite), each with its own settings and, if you wish, its own stretch of the video.
- **Regions.** Several per video, each either "filter inside" or "keep original". Keep original always wins. On a 360° video they sit on the sphere; on an ordinary video in the frame. They can move over time.
- **Flat view.** Cut an ordinary picture out of a 360° video, with the aim (yaw, pitch, roll and field of view) changing over time.
- **Audio ranges.** Mark stretches of the sound by hand and mute them, bleep them or disguise the voice. Everything is manual; nothing is detected for you.
- **Trim, presets and projects.** One trim range per video. Save a look as a preset and apply it to many recordings in a batch. Save and reopen a whole project as a `.mashbox` file.
- **Fast export.** Decoding, filtering and encoding overlap, and the filtering runs on the graphics card. Hardware encoders are used where the machine has them.

## Before you start

**ffmpeg.** Mashbox uses ffmpeg to read and write video, and does not include it. Install it once:

| System | Command |
| --- | --- |
| macOS | `brew install ffmpeg` |
| Windows | `winget install Gyan.FFmpeg` |

Mashbox looks for `ffmpeg` and `ffprobe` on your PATH and tells you plainly if it cannot find them.

**This build is not signed.** Your system will warn you the first time.

- **macOS:** open the app with right-click, then Open. [Fill in if the build is later signed and notarised.]
- **Windows:** at the SmartScreen warning choose More info, then Run anyway. [Fill in.]

Check the download against the checksum in the release notes if you want to be sure it is the file that was published.

## Things to know

- **Nothing leaves your computer.** Mashbox makes no network connections and sends no usage data. Your recordings are opened where they are; exports are written where you choose.
- **Exports always read your original recording.** A smaller preview copy may be made to keep playback smooth, but only when you ask for it, and it is never used for an export.
- **Voice disguise is not reliable anonymisation.** Mute and bleep are the safe modes. A disguised voice can sometimes still be recognised, and the app says so too.
- **Only mono video.** Stereo 360° video is not supported.
- **Source tags are dropped** from exports (for example location and title), and chapters are kept. A chapter title that names a person stays in the file.
- **Region names are saved as you type them** in projects and presets. Check that they do not name a participant before sharing a file.

## Use and licence

Terms of use will be added here before the first download is published.

## Problems and questions

Open an issue in this repository. Please do not attach recordings or anything that shows participants; describe what you did and what you expected, and say which system and Mashbox version you use.

## Citing

[Fill in once there is a DOI or a preferred reference.]
