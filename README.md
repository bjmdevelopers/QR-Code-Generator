# QR Code Generator

A free, fast, and 100% client-side QR code generator for URLs, text, email, phone, and WiFi. No backend, no tracking, no sign-up.

[![License: MIT](https://img.shields.io/badge/License-MIT-6366f1.svg)](LICENSE)
[![HTML5](https://img.shields.io/badge/HTML-5-e34f26?logo=html5&logoColor=white)](#)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6-f7df1e?logo=javascript&logoColor=black)](#)

---

## Features

- URL / Website — encode any link
- Plain Text — share notes and messages
- Email — optional subject and body
- Phone — one-tap dial via `tel:`
- WiFi — auto-connect with SSID, password and security
- Live Preview — regenerates as you type
- 3 Sizes — Small / Medium / Large
- Download PNG, Copy Image, Print
- Responsive and offline-ready
- Privacy-first — nothing leaves your browser

---

## Getting Started

```bash
git clone https://github.com/bjmdevelopers/QR-Code-Generator.git
cd QR-Code-Generator
```

- Open directly: double-click index.html
- Or run a local server (needed for the Copy feature):
  ```bash
  python -m http.server 8000
  ```
  Then open http://localhost:8000

---

## Deploy to GitHub Pages

1. Push to GitHub
2. Settings → Pages → Deploy from a branch
3. Select main / (root) → Save

Live at https://your-username.github.io/QR-Code-Generator/

---

## Tech Stack

- HTML5 + CSS3 (CSS variables, Flexbox) + Vanilla JavaScript (ES6)
- qrcodejs via CDN (with fallback)
- No build step, no dependencies to install

---

## Customization

Colors are CSS variables at the top of <style>:

```css
:root {
  --accent: #6366f1;
  --accent2: #818cf8;
  --bg: #f8fafc;
  --text: #1e293b;
  --radius: 16px;
}
```

## QR colors and error level in JS:

```js
new QRCode(qrContainer, {
  text: data,
  width: qrSize,
  height: qrSize,
  colorDark: '#1e293b',
  colorLight: '#ffffff',
  correctLevel: QRCode.CorrectLevel.H
});
```

---

## Encoded Formats

| Type | Format |
|---|---|
| URL | `https://example.com` |
| Text | Raw text |
| Email | `mailto:user@x.com?subject=Hi&body=Hello` |
| Phone | `tel:+919876543210` |
| WiFi | `WIFI:T:WPA;S:MyWiFi;P:pass123;;` |

---

## Notes

- Copy Image requires HTTPS or localhost (Clipboard API).
- Everything runs locally — no data is sent anywhere.
- Error correction set to H (30%) for reliable scanning.

---

Contributing

Fork, create a branch, commit your changes, and open a Pull Request. All contributions welcome.

---

License

MIT — see LICENSE.

---

Made with ❤️ and vanilla JavaScript.
