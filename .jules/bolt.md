## 2026-04-14 - WebViewer Lazy Loading
**Learning:** For static sites using heavy third-party libraries (like PDFTron WebViewer), loading the script unconditionally in the `<head>` blocks rendering and degrades initial load performance.
**Action:** Always implement a lazy loading pattern where heavy external libraries are dynamically requested via `document.createElement('script')` only when the user interacts with the specific component that requires it.
