# CreativeQR

**CreativeQR** is a client-side QR and barcode studio with a 3D visualizer and **Scanny**, a browser-based camera scanner.

**Creator & copyright holder:** Light Shadow Knight

## Live site

Once GitHub Pages is enabled for this repository, the site is published at:

**https://thelightwebofficial-cmyk.github.io/CreativeQR.github.io/**

The repository is configured for GitHub Pages with a GitHub Actions deployment workflow.

## Features

- QR code generation with configurable error correction
- 3D QR visualization with Forest, Ocean, and Stars environments
- Multiple 3D styles
- Code 128, Code 39, EAN-13, and UPC-A generation
- 2D PNG and 3D PNG export
- Scanny camera scanning using the browser Barcode Detection API when supported
- Safe review flow before opening scanned HTTP(S) links
- Fully client-side operation with no application backend
- Mobile-friendly interface and reduced-motion support

## Architecture

CreativeQR is intentionally packaged as a static site. The main application is contained in `index.html`, including the client-side QR/barcode logic and the inlined Three.js runtime used by the 3D scene.

There are no required runtime API keys or application servers.

## GitHub Pages deployment

The repository includes `.github/workflows/pages.yml`.

If the page is not appearing, check:

1. Open **Settings → Pages** in the repository.
2. Set **Source** to **GitHub Actions**.
3. Confirm Actions are enabled for the repository.
4. Open the **Actions** tab and check the **Deploy CreativeQR to GitHub Pages** workflow.
5. After a successful deployment, open the Live site URL above.
6. If a previous Pages deployment is cached, wait briefly and hard-refresh the page.

The repository already contains `.nojekyll` and a root `index.html`, so Jekyll processing is not required.

## Security

CreativeQR treats scanned QR/barcode data as untrusted input. Scanned content is displayed as text, links are not opened automatically, and the Safe Open action only permits HTTP(S) URLs.

See [SECURITY.md](SECURITY.md) for the security policy and deployment limitations of static hosting.

## Third-party notices

The application includes an inlined Three.js runtime. The embedded Three.js code is distributed under the MIT License. See [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

**Important:** The third-party Three.js component remains under its original third-party license. This does not grant any license to CreativeQR's original code, design, branding, or other original project material.

## License and ownership

CreativeQR's original application code, design, branding, documentation, and original creative assets are **All Rights Reserved** and are owned by **Light Shadow Knight**.

No permission is granted to copy, reproduce, modify, redistribute, publish, sublicense, sell, or create derivative works from the original CreativeQR material without prior written permission from the copyright holder.

Third-party components are governed only by their respective licenses.

See [LICENSE](LICENSE).

**Copyright © 2026 Light Shadow Knight. All rights reserved.**