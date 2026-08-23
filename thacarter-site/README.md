# Tha Carter Studios — demo site

A working demo to show Carter what the site can do. Not live copy — the photos
are his, everything else is a placeholder he can change.

---

## Put it on GitHub (5 minutes, from a phone or a laptop)

1. Sign in to **github.com** as `1stfloorproductions`.
2. **New repository** → name it `carter-demo` → **Public** → Create.
3. **Add file → Upload files** → drag in `index.html`, `404.html`, and the whole
   `assets` folder → **Commit changes**.
4. **Settings → Pages** → under *Branch* pick `main` / `/ (root)` → **Save**.
5. Two minutes later it's live at:
   **https://1stfloorproductions.github.io/carter-demo/**

That's the link to send Carter.

> A repo named `<username>.github.io` publishes automatically. Any other name —
> like `carter-demo` — needs step 4. That's the one people forget.

---

## What actually works in the demo

| Thing | Status |
|---|---|
| Live 24/7 dial in the hero | **Real.** Reads the visitor's clock, second marker sweeps. |
| Photo lightbox | **Real.** Tap any room photo. |
| Rate estimator | **Real math.** Room × hours + add-on, with a 10% discount past 8 hours. Prices are made up. |
| Media player | **Real interface, simulated audio.** Waveform, seek, playlist, auto-advance to the next track. No audio files loaded yet. |
| Booking form | **Front end only.** Validates and shows the confirmation. Nothing is sent anywhere. |

Everything degrades gracefully — with JavaScript off, all the content is still
readable. Keyboard accessible, respects reduced-motion, no horizontal scroll on
a phone.

---

## Going from demo to live

- **Delete the orange bar.** It's marked in `index.html` with a comment:
  `<!-- DEMO NOTICE — delete this whole <div> before going live -->`
- **Real prices** — in the HTML, `data-rate` on the three room buttons and
  `data-add` on the three add-ons.
- **Real tracks** — the `TRACKS` array near the top of the script. For actual
  playback, swap the simulated transport for an `<audio>` element.
- **The booking form** needs a back end. Cheapest routes: Formspree, Netlify
  Forms, or just point it at Carter's Calendly.
- **Social previews** — `og:image` is a relative path, which is fine for a demo.
  Live, make it the full `https://...` URL or Facebook won't pick it up.

---

## Files

```
index.html          the whole site — one file, no build step
404.html            wrong-door page
assets/logos/       the marks (SVG)
assets/photos/      Carter's photos, cropped and optimised
assets/fonts/       blackletter + caps, subset to 20 KB total
assets/og.png       social preview image
```

Fonts are self-hosted and subset — nothing loads from Google, so the page works
offline and there's no third-party request.

---

## Open questions for Carter

- Confirm the spelling: **Tha Carter Studios**.
- Does "by appointment only" belong on the public site, or just the door?
- Real rates, real room names, and which tracks he wants people to hear.
- Street address public, or on confirmation only?
