# TiltScroll Reader V1

A simple installable web app for tilt-controlled scrolling in a webpage frame or imported PDF.

## Important limitations
- iOS Safari requires a user gesture to request motion permission. Tap **Enable motion & start**.
- Motion sensors work only while the app page is open and active.
- Webpages are converted to a simplified text view through the third-party Jina Reader service. The page URL and request are sent to that service; some pages may fail to convert.
- Web reader requires internet access and the Jina Reader service. PDF rendering uses PDF.js from a CDN, so the first PDF load requires internet access.
- This app cannot inject scroll gestures into Apple Books, WhatsApp, Safari outside this app, or other apps.
- This is a prototype. Test tilt direction on your device and use the Direction selector if it feels inverted.

## Publish without a Mac (GitHub Pages)
1. On iPhone, open https://github.com and create/sign in to an account.
2. Create a new public repository named `tiltscroll-reader`.
3. Upload `index.html`, `manifest.webmanifest`, and `sw.js` to the repository root.
4. In the repository, open **Settings → Pages**.
5. Under Build and deployment, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, then Save.
6. Wait for GitHub Pages to publish. Your app address will look like:
   `https://YOUR-USERNAME.github.io/tiltscroll-reader/`
7. Open that address in Safari on your iPhone.
8. Tap Share → Add to Home Screen → Add.
9. Launch TiltScroll from the Home Screen. Open a PDF or webpage, then tap **Enable motion & start** and allow motion access if prompted.

## Use
- Web reader: enter an HTTPS URL and tap Open. Tilt scrolling works on the extracted reader text. The URL/page request is sent to Jina Reader.
- PDF reader: select a PDF from Files/iCloud Drive.
- Hold your phone in your normal reading position and tap Calibrate.
- Tilt gently. Adjust Sensitivity and Scroll speed.
- Tap Pause to stop motion scrolling.

## Privacy
PDF files are processed locally in the browser. Webpage URLs and page requests are sent to the third-party Jina Reader service to extract readable text. No analytics or app backend are included.
