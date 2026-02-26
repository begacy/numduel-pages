NumDuel screenshot mockups

Files in this folder are simple HTML templates sized for App Store screenshots.

Recommended export sizes:
- App Store (portrait): 1242 × 2688 px (iPhone 12 Pro Max / App Store full size)
- Play Store: 1080 × 1920 px

Exporting to PNG using Google Chrome (headless):

```bash
# macOS example (adjust path to Chrome binary if needed)
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless --disable-gpu --screenshot=../screenshot_01_setup.png --window-size=1242,2688 screenshot_01_setup.html
```

Or generate all screenshots with a small loop (bash):

```bash
for f in screenshot_01_setup screenshot_02_secret screenshot_03_voice screenshot_04_history screenshot_05_win; do
  "/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless --disable-gpu --screenshot=../${f}.png --window-size=1242,2688 $f.html
done
```

Alternative: use `wkhtmltoimage`:

```bash
wkhtmltoimage --width 1242 --height 2688 screenshot_01_setup.html ../screenshot_01_setup.png
```

If you want, I can attempt to render them here (requires headless Chrome installed in the environment). Otherwise download the generated HTML and run the commands locally, or I can provide exported PNGs if you give permission to attempt rendering.
