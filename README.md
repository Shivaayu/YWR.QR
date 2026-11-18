# YWR.QR — QR Code Generator (v1.0)

A responsive, static QR code generator intended for GitHub Pages. QR payloads are composed in the browser and are not sent to a YWR.QR backend.

## Current features
- URL, plain text, Wi-Fi, vCard contact, email, phone, WhatsApp and SMS QR payloads
- Foreground/background colour, output size and error correction selection
- Optional centre logo upload (processed locally in the browser)
- PNG download and image copy where supported
- Responsive mobile/desktop layout

## Run locally
Open `index.html` in a modern browser while connected to the internet. The QR engine is loaded from cdnjs (QRCode.js 1.0.0). The page does not send the entered QR content to cdnjs; only the library script is fetched. Google Fonts are also loaded remotely for typography.

## Publish on GitHub Pages
1. Create a public GitHub repository, for example `ywr-qr`.
2. Upload `index.html`, `styles.css`, `app.js` and this README to the repository root.
3. Open **Settings → Pages**.
4. Under Build and deployment, choose **Deploy from a branch**, select `main` and `/ (root)`, then Save.
5. Wait for GitHub Pages to publish the site. The address will usually be `https://YOUR-USERNAME.github.io/ywr-qr/`.

## Important technical notes
- This v1 uses QRCode.js from cdnjs as a browser-side generation library. For a fully self-contained/offline build, vendor a reviewed copy of that library into the repository and retain its applicable license notice. The current build requires internet access to load the QR engine.
- The current export is PNG. SVG export is not included in this first version.
- Logo overlays can reduce scan reliability. High error correction is selected by default; always test a logo QR with more than one scanner before sharing.
- Static QR codes encode their content directly. If a destination changes, the QR must be regenerated.
- No analytics, accounts, database, tracking scripts or YWR.QR application backend are included.

## Third-party components
- QRCode.js 1.0.0, loaded from cdnjs: https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js
- DM Sans and Space Grotesk fonts, loaded from Google Fonts. System sans-serif fallback is used if unavailable.

Before public launch, verify the exact third-party license notices and decide whether to bundle dependencies locally. Do not claim complete offline operation until the QR library is bundled.
