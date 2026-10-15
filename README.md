# MergeFlow — Merge PDFs privately

A single-page web app that merges any number of PDF files into one, entirely in your browser. No uploads, no servers, no tracking.

## Features

- **Merge unlimited PDFs**: add as many files as you like, all at once or a few at a time
- **Drag & drop or browse**: drop files anywhere on the card, or click to select multiple files
- **Reorder easily**: drag rows to rearrange, or use the up/down arrows (handy on mobile)
- **Remove files**: delete a single file or clear the whole list
- **Page counts**: see each file's size and pages, plus a running total
- **Preview**: flip through the merged result before downloading
- **Custom filename**: name the output file anything you want
- **Private by design**: files are processed locally and never leave your device
- **Responsive**: works on desktop and mobile

## How to use

1. Open `index.html` in a browser (or visit the hosted page).
2. Drop in your PDFs, or click the drop area to choose them.
3. Arrange them in the order you want. Files are merged top to bottom.
4. Optionally change the output filename.
5. Click **Merge PDFs**, then **Preview** or **Download PDF**.

At least two PDFs are needed to merge.

## Running locally

No build step or dependencies to install. Just open the file:

```bash
git clone https://github.com/ishitadutta2/MergeFlow.git
cd MergeFlow
open index.html        # macOS; on Linux use xdg-open, on Windows use start
```

An internet connection is needed on first load, since the libraries and fonts come from CDNs.

## Deploying

It is one static HTML file, so it works on any static host. For GitHub Pages: go to **Settings → Pages**, choose the `main` branch and the root folder, and save. The site will then be live at https://ishitadutta2.github.io/MergeFlow/.

## Built with

- [pdf-lib](https://pdf-lib.js.org/) 1.17.1 to merge the PDFs
- [PDF.js](https://mozilla.github.io/pdf.js/) 3.11.174 to render the preview
- Vanilla HTML, CSS and JavaScript, with no framework
- Fonts: Source Serif 4 and JetBrains Mono (Google Fonts)

## Limits and notes

- Each file can be up to **50 MB** (change `MAX_MB` in `index.html` to adjust it).
- Very large merges use your browser's memory, since everything happens in the tab.
- Password-protected or corrupted PDFs can't be read and are rejected with a message.

## Privacy

Your files never leave your browser. Nothing is uploaded, stored, or sent anywhere. Closing or refreshing the tab discards everything.
