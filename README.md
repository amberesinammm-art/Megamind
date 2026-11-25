# MEGAMIND — Video Clipping Studio

A browser-based video trimmer. Upload a video, choose start/end times, and export the selected section as an MP4.

## Run locally

Because the app loads FFmpeg WebAssembly as an ES module, serve the folder over HTTP (not by opening the HTML file directly).

With Python:

```bash
python -m http.server 8000
```

Then visit http://localhost:8000.

## Deploy with GitHub Pages

1. Open the repository **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select **main** and **/(root)**, then Save.
4. Wait for the Pages deployment to finish. Your site will be available at `https://amberesinammm-art.github.io/Megamind/`.

## Notes

- Video processing runs in the user's browser with FFmpeg WebAssembly. Source videos are not uploaded to a MEGAMIND backend.
- Large files can consume significant browser memory; shorter/smaller source files are recommended for the first version.
- FFmpeg assets are loaded from jsDelivr, so an internet connection is required.
- This MVP supports basic trim/export. Automatic AI highlight detection, accounts, cloud storage, and advanced aspect-ratio editing are not included yet.
