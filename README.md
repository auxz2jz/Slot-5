# OpenFFmpeg Web

A self-contained browser-based FFmpeg interface using ffmpeg.wasm. Media processing happens locally in your browser.

## Run it

### GitHub Pages
This repository already contains the web interface and the FFmpeg WebAssembly runtime it uses. The app does not need to download its runtime from a CDN.

Open the repository's GitHub Pages site, press **Load FFmpeg Engine**, choose a media file, and convert it.

### Download the complete project
Use GitHub's **Code → Download ZIP** button. The download includes the OpenFFmpeg Web interface, the local browser runtime under `vendor/ffmpeg/`, and the vendored upstream source snapshots under `_source/`.

> Opening `index.html` directly with `file://` may still be blocked by browser WebWorker/WebAssembly security. GitHub Pages or another local HTTP server avoids that browser restriction.

## What it does
- Video output: MP4, MKV, WebM, MOV
- Audio output: MP3, WAV, FLAC
- Animated GIF
- Quality presets
- Resolution presets through 4K
- Audio bitrate controls
- Remove audio
- Trim start/end
- Advanced FFmpeg arguments
- Progress, cancel, activity log, preview, and download

## Local FFmpeg runtime
The running application loads only files stored in this repository:

- `vendor/ffmpeg/ffmpeg.js`
- `vendor/ffmpeg/814.ffmpeg.js`
- `vendor/ffmpeg/ffmpeg-core.js`
- `vendor/ffmpeg/ffmpeg-core.wasm`

Pinned runtime versions are recorded in `vendor/ffmpeg/VERSIONS.txt`.

## Full upstream source snapshots
`_source/` contains complete tracked working-tree snapshots of:

- `FFmpeg/FFmpeg`
- `ffmpegwasm/ffmpeg.wasm`
- the `ffmpegwasm/testdata` submodule used by ffmpeg.wasm

Nested `.git` metadata is intentionally not copied, so `Slot-5` remains one normal Git repository. `_source/SOURCE_INFO.md` records the exact upstream commit IDs copied into this repository.

The full source is included for preservation/reference. The web app itself runs from the local prebuilt runtime in `vendor/ffmpeg/`.
