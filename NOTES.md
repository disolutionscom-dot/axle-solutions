# Axle Solutions — Website (axlesolutions.ae)

Single-file static site. Deploy by dragging this folder to Cloudflare Pages / Vercel / Netlify / GitHub Pages.
Files: `index.html` + `img/`. No build step. Uses anime.js + Lenis via CDN (needs internet when viewed).

## Built per WEBSITE-BLUEPRINT.md
Sections: loader · nav · hero · about · capabilities (tabs) · benefits · services · process ·
gallery (lightbox) · testimonials · FAQ · CTA · contact (form + live map) · footer · float CTA.

## Firdous logos removed
All competitor "FIRDOUS METALIC IND" logos were removed from the supplied photos
(cropped on w05; content-aware inpaint on w06/w08/w09). The competitor marketing
flyer and a duplicate were dropped. Gallery/tab images = img/g1–g9.jpg + hero-weld.jpg.

## Hero background — canvas frame animation (always plays)
The hero background is **no longer a `<video>`**. A `<video>` can always be blocked by the
device (iOS/macOS Low Power Mode, Safari "never auto-play", data-saver) and no code can force
it — that's why you kept having to tap.

Instead the laser footage is now 48 frames packed into one sprite sheet
(`img/laser-frames.jpg`, ~450 KB) drawn on a `<canvas>` and played forward-then-reverse
(ping-pong) at 12 fps. **Canvas drawing is never subject to autoplay policy**, so it starts on
its own, every time, on every device — no tap, no permission. At 0.68 opacity behind the dark
overlay. The old `img/hero-laser.mp4` is now unused (kept in the folder in case you want it).
To use a different clip later, send it and I'll re-generate the sprite sheet.


## Logo
Your logo kept arriving pasted **inline (not as a file)**, which I can't read pixel data from —
so I traced it into a clean, scalable **SVG** (`img/axle-logo.svg`): red gear, AS monogram,
laser nozzle + spark. It's placed **everywhere**: nav, footer, page-loader, browser favicon,
and the SEO/schema logo. It's a faithful recreation, not a pixel copy — if you can save the
official logo as a **PNG/SVG file** into Downloads, I'll swap in the exact artwork.

## Parent companies — Firdous Steel & Taj Al Mas
Axle Solutions is shown as backed by its two parent companies. Reflected in:
- About: "Backed by Firdous Steel & Taj Al Mas" tag + copy.
- Footer: "Our Group" column → Firdous Steel (firdoussteel.com) + Taj Al Mas (tajalmas.com).
- Copyright: "a Firdous Steel & Taj Al Mas group company".
(Note: Firdous logos were still removed from the *photos* earlier — that's fine, the photos
are logo-free; this just credits the parent companies in text.)

## Clever categorisation — "What We Fabricate" (9 categories)
Replaced the old 4-tab section + services block with one clean 9-category grid built from the
group's real specialisations: SS Kitchens · Laser & Sheet Cutting · SS Cladding · Structural
Fabrication · Aluminium Fabrication · Handrails & Balustrades · SS & GI Ducting · Hospital &
Lab Furniture · Custom Metal Works.

## Category images sourced from the internet (Pexels — free commercial, no attribution)
Your own cleaned photos cover Kitchens (g1), Ducting (g3), Hospital (g6), Custom (g8).
For categories you had no photo of, I pulled representative Pexels stock: cat-laser (commercial
laser cutting steel sheet), cat-clad (steel/metal cladding facade), cat-struct, cat-alu, cat-rail
(stainless-steel railing — no glass). These are ILLUSTRATIVE capability images, not claimed as
your specific completed projects (your real work stays in the "Projects" gallery). Replace any
with your own site photos whenever you have them.

## Clients strip — REMOVED
The "Trusted by leading brands" client strip was removed at your request (no permission to
display those client names). Section, nav link and JS all deleted.

## Design language
Rebuilt as an industrial/editorial system (not a generic template): Anton condensed display
type, solid headings with a single red accent word, flat steel panels with hairline borders,
red section rules, no rainbow gradients. Fonts: Anton + Archivo + Inter.

## ⚠️ PLACEHOLDERS — please confirm / edit before going live
- Hero stats: 10+ years, 1,200+ projects, 150+ clients — sample figures. Update in index.html (#heroStrip / data-n).
- Testimonials: 3 sample quotes (initials only) — replace with real client feedback (TESTIMONIALS array).
- WhatsApp FAB link uses the landline (+971 6 742 9921). A landline can't use WhatsApp —
  give me your WhatsApp mobile number and I'll fix the wa.me link.
- Address: "Sharjah — U.A.E." (inferred from 06 area code) + map query. Confirm exact address.
- LOGO: your new logo was pasted into chat as an inline image, not a file, so I can't read its
  pixels to place it on the site. Please drop the logo **PNG (transparent background)** into your
  Downloads folder and I'll wire the real one into the nav/footer. (Current logo is still the older
  cropped version.) An SVG recreation was attempted but looked worse, so it was discarded.
- Contact form uses a mailto: fallback (opens the visitor's email app). For direct-to-inbox
  submissions, connect Formspree/Getform or a backend.

---

## UPDATE — 2026-07-19 (major revision)

**Focus shifted to LASER CUTTING + architectural/structural steel. Kitchen removed entirely.**

- **Logo = your EXACT logo.** Extracted as vector from `axle solutions working 1.pdf` (it was
  vector art, not a photo), background keyed to transparent. `img/axle-emblem.png` (gear + AS +
  laser spark) is used in nav, footer, loader, favicon; `img/axle-logo.png` (full lockup with
  wordmark) is the SEO/schema logo and is available for print. The earlier hand-drawn SVG is gone.
- **Hero** now leads with laser: "Precision laser cutting & metal fabrication", kicker "20 kW
  Fibre Laser · 2m × 6m Bed", real stats (20 kW, 14+ yrs, 200+ clients GCC-wide, 40 machines —
  all from the Taj Al Mas brochure). Background **video opacity raised to 0.68** with a lighter
  overlay so the laser footage shows through clearly.
- **12 service categories** (was 9, no kitchen): Laser Cutting · Mashrabiya & Decorative Panels ·
  Base Plates & Flanges · Pipe & Section Rolling · Handrails & Staircases · Bollards & Posts ·
  Fencing & Steel Gates · Structural Steel · Fabrication & Lathe Work · Cladding & Profiles ·
  Custom Fabrication & Welding · Pergolas & Canopies.
- **Real images** now used throughout — pulled from the Taj Al Mas brochure (laser 20 kW, handrails,
  bollards, gates, structural, profiles, bending/shearing machines) and the Dawar Al Falah brochure
  (mashrabiya panel, brass flanges, lathe/turned parts). Projects gallery + testimonials + FAQ +
  contact-form options all rewritten around these services.
- **Parent companies:** About credits **Firdous Metalic Ind. LLC** & **Taj Al Mas Group** (full
  names). Footer group column shows **Taj Al Mas Group only** (Metal Fabrication & Welding LLC +
  Eng. Turning); copyright reads "part of Taj Al Mas Group".

### ⚠️ Confirm before publishing
- **Image rights:** the mashrabiya / flanges / lathe images come from the **Dawar Al Falah**
  brochure and some Taj Al Mas brochure photos may be stock the group licensed. Fine if these are
  sister/group companies and you have rights — please confirm, or send me your own photos to swap in.
- Stats (200 clients, 14 yrs, 40 machines, 20 kW / 2×6 m) are taken from the Taj Al Mas brochure —
  confirm they apply to Axle Solutions specifically.
- WhatsApp button still uses the landline; send a mobile number.

## UPDATE — 2026-07-19 (later)
- **Parent company = Taj Al Mas ONLY.** Firdous removed completely (0 refs on page). The
  **Taj Al Mas Group logo** was extracted from the Taj Al Mas brochure PDF, background keyed
  transparent (`img/taj-logo.png`), and shown as a "Part of [logo]" badge in About + footer.
- **Hero background is now a CANVAS animation, not a video** (see "Hero background" section
  above) — it always plays automatically, no autoplay blocking possible.
