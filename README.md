# OpenFFmpeg Web

A browser-based FFmpeg interface using ffmpeg.wasm. Media processing happens locally in your browser.

## Run it

### Easiest: GitHub Pages
1. Open this repository on GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Choose the default branch and `/ (root)`, then save.
5. Open the GitHub Pages address GitHub gives you.
6. Press **Load FFmpeg Engine**, choose a media file, and convert it.

### Download the files
Use GitHub's **Code → Download ZIP** button, extract the ZIP, and keep `index.html`.

> Important: double-clicking `index.html` may be blocked by browser WebWorker/WebAssembly security when opened as `file://`. Hosting it with GitHub Pages avoids that problem.

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

## FFmpeg engine
The page loads the browser-compatible ffmpeg.wasm engine over the internet. It does not upload your media to GitHub for conversion; processing happens in the browser.
