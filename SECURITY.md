# Security Policy

CreativeQR treats QR and barcode payloads as untrusted input.

- Scanned values are rendered as text rather than executable HTML.
- Scanned links are never opened automatically.
- Safe-open is restricted to HTTP(S) URLs.
- Camera access is requested only when Scanny is opened.
- Input sizes and generation frequency are limited client-side.
- No API secrets are embedded in the application.

GitHub Pages is static hosting. It cannot provide server-side WAF, authentication, backend isolation, or server-side rate limiting. Add those controls at the edge/backend if a server is introduced later.

Copyright © 2026 CreativeQR. All rights reserved.
