# YWR.QR — QR Code Generator

A static, mobile-responsive QR code generator. The project runs on GitHub Pages and does not require a personal server, database, account system or paid API.

## Files

- `index.html` — page structure
- `styles.css` — responsive interface
- `app.js` — QR content formatting, validation, generation and downloads

## Run locally

Keep all three files in the same folder and open `index.html` in a modern browser. An internet connection is currently required to load the QRCode.js library from jsDelivr (with cdnjs as a fallback). Google Fonts are optional; the page falls back to system fonts.

## Publish with GitHub Pages

1. Create a public repository named `ywr-qr`.
2. Upload the **contents** of this folder (`index.html`, `styles.css`, `app.js`, `README.md`) to the repository root. Do not upload only `index.html`.
3. Open repository **Settings → Pages**.
4. Under Build and deployment, select **Deploy from a branch**.
5. Select branch `main` and folder `/ (root)`, then Save.
6. Wait for GitHub Pages to publish the site.

## Features

- Website URL, plain text, Wi-Fi, vCard contact, email, phone, WhatsApp and SMS QR payloads
- Foreground/background colour, image size and error correction settings
- Optional centre logo upload (PNG, JPG or WebP, up to 2 MB)
- PNG download and clipboard image copy where supported
- Browser-side payload handling; content is not sent to a YWR.QR server

## Third-party library and licensing

QR generation uses QRCode.js by davidshimjs, distributed under the MIT License. The library is loaded from a public CDN at runtime. See https://github.com/davidshimjs/qrcodejs and https://github.com/davidshimjs/qrcodejs/blob/master/LICENSE.

The YWR.QR project interface and application code are separate from the third-party QR library. Keep the library's copyright and license notice if you later bundle or redistribute its source file.

## Important limitations

- QR codes generated here are static. Editing the destination after printing is not supported.
- Dynamic redirects, scan analytics, user accounts and cloud sync are not included.
- Wi-Fi QR compatibility depends on the phone's camera/scanner and network configuration.
- A logo can reduce scan reliability. Test every generated code on more than one scanner before printing or sharing.
- QR content is not automatically checked for malicious or unsafe destinations. Review links before opening them.
