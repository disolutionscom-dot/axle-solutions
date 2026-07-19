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

## Hero background video
`img/hero-laser.mp4` — your Vecteezy laser-cutting clip. Hero is **video only** (no picture)
at **0.5 opacity (50% transparent)**. Autoplays muted and runs as a **ping-pong loop**: plays
forward, then rewinds at 1x back to the start, then forward again, forever (JS-driven, since
HTML video can't play in reverse natively).
Now **compressed to ~4.3 MB** (720p, H.264, **audio track removed**, faststart) — down from
16 MB. Removing the audio track + shrinking the file is what makes muted autoplay reliable;
the JS also retries repeatedly and starts on the first interaction anywhere as a fallback.
If autoplay STILL needs a click on a given device, that's the browser/OS blocking it
(Safari "Never Auto-Play" setting, or Low Power / battery-saver mode) — no website can
override those; the click fallback covers it.
The clip is 23.7 s, so the ping-pong cycle (forward + reverse) is ~47 s. Say the word and I'll
trim it to a punchier ~8–10 s loop. Vecteezy free clips need attribution unless you hold a Pro
licence — confirm your licence.

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
