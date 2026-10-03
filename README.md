# ConvertFlow

**A fast, private image ↔ PDF converter that runs entirely in your browser.**

Turn photos into a clean PDF, or save PDF pages as images, with no sign-up, no uploads, and no server. Your files never leave your device.

---

## Features

### Images → PDF
- Add multiple images at once (JPG, PNG, WEBP, GIF, BMP) via drag and drop or file picker
- Reorder pages with simple move up / move down controls
- Choose the page size: **A4**, **US Letter**, or **same as image**
- Adjustable margins (none, small, large)
- Five quality levels, from *Best* to *Smallest*
- **Keep file under…** option (100 KB to 5 MB): automatically compresses the PDF until it fits, which is handy for upload forms with size limits
- Transparent PNGs are flattened onto a white background

### PDF → Images
- Convert every page, or choose specific pages (e.g. `1-3, 5`)
- Export as **JPG** (smaller files) or **PNG** (sharper text)
- Four resolution levels, from *Screen* to *Print quality*
- Multi-page results are bundled into a single **ZIP** download
- Thumbnail previews of converted pages
- Clear messages for password-protected or unreadable PDFs

### Experience
- Responsive layout that works on phones, tablets, and desktops
- Automatic light and dark mode
- Keyboard accessible, with progress feedback during conversion
- Single self-contained HTML file with no build step

---

## Privacy

All processing happens locally in your browser using the Canvas API and client-side libraries. No file is uploaded, stored, or sent to any server.

---

## Getting Started

**Option 1: Open directly**

1. Download `index.html`
2. Open it in any modern browser (Chrome, Edge, Firefox, Safari)

**Option 2: Host it**

Because it is a static page, it works on GitHub Pages, Netlify, Vercel, or any static host:

1. Go to **Settings → Pages** in your repository
2. Select the branch and root folder
3. Your converter will be live at `https://<username>.github.io/<repo>/`

> An internet connection is needed on first load so the libraries below can be fetched from their CDNs.

---

## Usage

**Images → PDF**
1. Drop your images in, or click to choose them
2. Arrange the order, then pick page size, margin, and quality
3. Optionally set a maximum file size
4. Click **Create PDF**, then **Download**

**PDF → Images**
1. Drop in a PDF
2. Choose format, resolution, and (optionally) a page range
3. Click **Convert to images**, then **Download**

---

## Built With

| Purpose | Library |
|---|---|
| PDF creation | [pdf-lib](https://pdf-lib.js.org/) |
| PDF rendering | [PDF.js](https://mozilla.github.io/pdf.js/) |
| ZIP packaging | [JSZip](https://stuk.github.io/jszip/) |
| Image processing | Browser Canvas API |

Plain HTML, CSS, and vanilla JavaScript. No framework and no build tools.

---

## Limitations

- Very large images are scaled down to avoid running out of browser memory
- Password-protected PDFs are not supported
- Output size depends on image content; extremely small size limits may not always be reachable

---

## Roadmap

- [ ] Drag-to-reorder pages
- [ ] Image rotation before export
- [ ] Manual dark / light theme toggle
- [ ] Offline support (PWA)

---

## Contributing

Issues and pull requests are welcome. For larger changes, please open an issue first to discuss what you would like to change.

---

## License

Released under the [MIT License](LICENSE).
