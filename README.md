# Threds Webflow Static Export

This folder is a direct static export of https://threds.webflow.io/ prepared for deployment on Vercel.

No pages have been rebuilt, redesigned, or converted to React. The Webflow-exported HTML, CSS, JavaScript, images, documents, videos, and asset folders are intended to stay in place.

## Project Structure

- `index.html` is at the project root and is the static homepage.
- Other HTML pages are also at the project root.
- Static assets are kept in:
  - `css/`
  - `js/`
  - `images/`
  - `documents/`
  - `videos/`
- `MISSING.txt` is preserved because the Webflow export reported missing assets.

## Deploying To Vercel

1. Create a new Vercel project from this folder.
2. Use the project root as the Vercel root directory.
3. Use the static/Other framework preset.
4. Leave the build command empty.
5. Leave the output directory empty, or use the project root if Vercel asks for one.
6. Deploy.

The included `vercel.json` enables clean URLs, so pages such as `about.html` can also be served as `/about`.

## Missing Assets Reported By Webflow

`MISSING.txt` lists these assets as failed downloads during export:

- `videos/Video-for-homepage-online-video-cuttercom-1-transcode.webm`
- `videos/features-bottom-transcode.mp4`
- `videos/features-bottom-transcode.webm`
- `videos/features-bottom.mp4`
- `videos/features-top.mp4`
- `videos/thredx-about-video-transcode.mp4`
- `videos/thredx-about-video-transcode.webm`
- `videos/thredx-about-video.mp4`
- `videos/thredx-video-header-1-transcode.mp4`
- `videos/thredx-video-header-1-transcode.webm`

These files were not replaced with placeholders.

## Additional Missing Local References Found

The local asset scan found this missing image reference:

- `blog.html` references `images/Arrow-btn_1Arrow-btn.png`
- `detail_blog-posts.html` references `images/Arrow-btn_1Arrow-btn.png`

The closest existing asset is `images/Arrow-btn_1Arrow btn.png`, but no rename or replacement has been made.

## Internal Links

Internal HTML page links were checked and all referenced pages exist in this export.

The current HTML still uses Webflow's exported `.html` links, such as `about.html` and `features.html`. These links work on Vercel, and `vercel.json` also enables clean URL access such as `/about` and `/features`.
