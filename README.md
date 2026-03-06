# Mato Pitch Deck

HTML pitch deck for Mato. View in a browser or export to PDF.

## Generate PDF

From this directory (`pitch-decks`), run:

```bash
cd pitch-decks
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless --disable-gpu --no-pdf-header-footer --print-to-pdf=mato-pitch.pdf "file://$(pwd)/mato-pitch.html" 2>/dev/null
```

**Requirements**

- **macOS:** Google Chrome installed at the default path above.  
  If Chrome is elsewhere, use that path instead of `"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome"`.
- **Linux:** Use your Chrome or Chromium binary, e.g.  
  `google-chrome` or `chromium-browser` instead of the macOS path.

**What it does**

- Renders `mato-pitch.html` in headless Chrome and prints to PDF.
- Output file: `mato-pitch.pdf` in the same directory (overwritten each run).
- `2>/dev/null` hides headless Chrome log messages (e.g. display warnings).

**One-liner from repo root**

If you’re in the repo root and `pitch-decks` is a subdirectory:

```bash
cd pitch-decks && "/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless --disable-gpu --no-pdf-header-footer --print-to-pdf=mato-pitch.pdf "file://$(pwd)/mato-pitch.html" 2>/dev/null
```

Replace the quoted Chrome path if needed for your OS or install location.
