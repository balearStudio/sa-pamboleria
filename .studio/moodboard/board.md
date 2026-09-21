# Sa Pamboleria — reference board

Inca, Mallorca · assembled 2026-09-20 · read this cold, without the conversation that made it.

This board collects **references and evidence**. It does not choose a palette, typefaces, a
layout or a motion idea — those are decided at `/ewf:design`, from the brief, the photographs
and this board. Nothing here was copied from any site: no layout, no asset, no wording.

---

## The client's subject, in a sentence

A family-run Mallorcan restaurant named after **pa amb oli** — they make thirteen versions of
it — that also runs a charcoal grill, and serves both from a **covered terrace under thatched
palm-frond parasols** in a residential neighbourhood of Inca, to locals who review them in
Catalan and talk about portions rather than presentation.

The two most characteristic things they own are **the rubbed-tomato bread built thirteen ways**
and **that terrace**. Neither appears on any competitor's site.

---

## References

### 1. Da Maria — the owner's lead reference
`https://damaria-roma.webflow.io` · Roman restaurant · `refs/damaria/`
Intake records this as the owner's pick "for the site as a whole".

**Take:** the **keyline frame** — a single thin rule boxing the entire page, inset from the
viewport edge, so the page reads as a printed menu card rather than a web page. Sa Pamboleria's
only real brand artefact is a printed menu, so the device is already theirs in spirit.
Secondary: **engraved line illustration** used as a recurring motif (a menu on a plate, a
telephone, oysters), and **drop caps** opening body paragraphs — structure coming from
typography instead of from more cards. Its display type is set enormous, around 245px, and
allowed to bleed off both edges.

**Leave:** its red-on-cream at body size fails contrast where it is used (measured 4.1:1 and
4.36:1 against a 4.5 floor), and its shop row and founder's note have no equivalent here.

### 2. Etxebarri — international best-in-field
`https://asadoretxebarri.com` · Axpe, Bizkaia · `refs/etxebarri/`
The reference point for charcoal-grill dining anywhere.

**Take:** **it opens on the building, not the meat** — a stone wall, a window, a grill pan on a
hook — with the wordmark small and white in the corner. The most famous grill restaurant in the
world leads with *place*. That is permission for Sa Pamboleria to lead with its terrace.
Also: display type set very large and very *light* over a quiet neutral text face, and
practical facts (price, covers, what's excluded) handled as icon + label + one short paragraph
in two columns rather than as a bullet list — Sa Pamboleria has exactly that kind of content
in parking, terrace, berenar hours and "no bookings".

### 3. Caffè Gilli — adjacent field: the historic family establishment
`https://www.caffegilli.com/en` · Florence, est. 1733 · `refs/caffegilli/`
Awwwards honourable mention. A traditional family café presented contemporarily — the same
problem Sa Pamboleria has.

**Take:** **hands in the frame, doing the work.** A hand piping cream onto a pastry; a hand
reaching for the plate on a marble table. Warm low light, shallow depth. It is the most direct
evidence that the owner's hero instinct is right, and that it works photographically on a real
shipped site rather than only as an illustration. Also: a small oval wordmark held quietly at
top centre, and an `/en` language structure for a multilingual traditional business.

**Leave:** a cookie wall covers a third of the landing view.

### 4. Bunbite + Tacos My Guey — the owner's other two references, one point
`https://dribbble.com/shots/27022855` · `https://tacosmyguey.com` · `refs/bunbite/`, `refs/tacosmyguey/`

**Take — one thing, and the reason it matters:** both show **food cut out of its background and
floated on a flat colour field**, and Bunbite shows it as **a hand holding the food**. Put
beside Caffè Gilli, this is the thread running through *all three* of the owner's references.
Their hero idea is not a whim; it is the one move their taste keeps returning to, and the board
should treat it as a standing request rather than a preference to be talked out of.

**Leave:** Tacos My Guey sets body text in condensed display caps and has measurable horizontal
overflow at desktop; Bunbite is an unbuilt concept shot with starburst badges and a rewards
economy. Take the product treatment, nothing else.

### 5. Son Daven — international, regional culture made contemporary
`https://sondaven.com/en` · Carpathians · Awwwards Site of the Month, June 2026
**No screenshot: the site is WebGL-heavy and defeated three capture attempts.** Recorded from
its Awwwards entry, so treat it as weaker evidence than the four above.

**Take:** the positioning problem solved well — *regional culture meeting contemporary
hospitality* without turning the region into rustic decoration. Reported as a two-colour scheme
of warm taupe against deep charcoal, with illustration used as a structural layer alongside
photography. Worth a look at `/ewf:design` if it can be opened directly.

---

## The competitor line

**Cas Teuler** — `https://www.casteuler.com/carne/` · `refs/casteuler/` · a Mallorcan
charcoal-grill restaurant, the nearest same-island, same-trade business with a real website.
Looked at once, as a constraint.

**How Sa Pamboleria differs:**

1. **Their hero already says "CARNES A LA BRASA"** — the same sentence as Sa Pamboleria's own
   printed logo line. The clash is the *proposition*, not the styling. Any direction that leads
   on grilled meat is the second Mallorcan restaurant saying the same thing, and the one with
   worse photography: Cas Teuler has commissioned studio work (a chuletón over live flames,
   backlit), Sa Pamboleria has flat-lit phone shots at 1080px.
2. **They have no pa amb oli and no place.** No bread, no terrace, no daylight, no people. Both
   of Sa Pamboleria's genuinely characteristic assets are ground the competitor cannot stand on.
3. **They have no typographic voice** — h1 at 20px, tracked-out caps eyebrows above every
   heading, a nine-up grid of near-identical dark meat shots, a copper gradient footer.

Matching them makes Sa Pamboleria look like their weaker copy. The differentiation is
**the bread and the terrace**, not a better version of their fire.

---

## Material and colour evidence from the client's own photographs

Sampled from the pixels, with sources. **This is evidence, not a palette** — `/ewf:design`
decides what, if anything, to do with it.

**The wordmark — `images/logo-source-isolated.png` (+ `-alpha.png`, `-balanced.png`).**
Sa Pamboleria has no vector logo, no brand guide and no transparent asset. The wordmark
survives only as printed artwork inside a photograph of the menu
(`.studio/assets/menu/menu-page-1.png`). That photograph is heavily blue-cast — the paper,
which is white, was captured at `#A6B9EE`. White-balancing against the paper's own white point
recovers the ink as a **slate navy around `#364966`**, core `#2E4162`.

The full lockup is a brush script reading **Sa Pamboleria**, with a sprout above the "o" and a
swash underline, **"TERRASSA · PA AMB OLI"** curved above, **"CARNS A LA BRASA"** curved below,
and a dot flanking each side. Measured ink area in the source photograph: **447 × 350 px** —
small, and the reason a clean vector is needed.

Three prepared files, all cropped to the **complete** lockup with nothing clipped:
- `logo-source-balanced.png` — white-balanced, otherwise untouched. Keeps the paper texture and
  the watercolour wash behind the mark. Truest to the original.
- `logo-source-cleaned.png` — the same with gentle levels, paper lifted toward white.
- `logo-source-isolated.png` / `-alpha.png` — **the navy ink alone**, the watercolour olive
  branch and the vegetable illustration masked out, composited on white and as RGBA.
  **This is the file to hand to Magnific**, because the wash would otherwise be upscaled as
  though it were part of the mark.

**The only real brand identity that exists**, and the only handwritten element the site should
contain — whatever typeface the design chooses, nothing else on the page should be a script.

**The terrace — `.studio/sources/images/ig-02.jpg`.** The richest frame in the pack and the
biggest thing the research brief undersold: thatched palm-frond parasols, rustic olive-wood
furniture, gravel underfoot, white tablecloths, palms and olive trees, pale cream walls.
Sampled: olive wood `#735F41`, gravel `#846B49`, thatch `#43331B`, cream wall `#DBC090`,
foliage `#6B7635`, tablecloth white `#FBFBF7`. **Two cautions:** the script wordmark is baked
into this frame as a large white overlay, and `fb-01` is the same photograph — so this is the
*only* usable terrace shot, and using it as a hero means painting the overlay out.

**The grill — `ig-09.jpg`.** The sharpest file in the pack and the only one shot on a dark
ground: dry-aged beef on black slate with salt flakes. Sampled: slate `#070307`, aged burgundy
`#8E4C56`, salt `#EBEBEE`.

**The food generally — `ig-12`, `ig-14`, `ig-30`.** Overwhelmingly warm: 88–94% of pixels fall
in the red-to-amber band. Sampled: sobrassada red `#9E2124`, ember `#D88047`, oil amber
`#D5A761`, bread `#B77348`.

**What the pack cannot do:** 22 usable images, all phone-shot at 1080px (1170 max), flat-lit and
cropped hard to the frame edge. **No dessert photograph exists** although four homemade cakes
are on the menu. **No usable photograph of a person** — the one that exists shows an
identifiable customer. If the design wants people or desserts, they have to be produced.

---

## Image ideas for `/ewf:design` to consider — requests, not work

1. **The owner's hero: a cut-out pa amb oli, ideally with a hand reaching for it.** Standing
   request, reinforced by all three of their references and by Caffè Gilli.
   *Feasibility was tested out-of-stage and is known:* `ig-11` (lamb chops on pa amb oli, plate
   rim visible on three sides) enhances well — a Magnific 2× pass at €0.0024 produced a sharper,
   truer file with nothing invented, kept at `images/ig-11-upscaled.jpg`. Magnific's
   **background-removal endpoint returns HTTP 403 on this API key**, so a local saturation mask
   was used instead; it isolates **the food without its plate**, and reads well on a dark field
   (`images/cutout-on-dark.jpg`). So the cut-out is achievable, as a plateless food object
   rather than a cut-out plate. **No hand-reaching photograph exists in the pack.**
2. **A clean vector wordmark.** Blocking for any direction that shows the logo large. Cheapest
   and best route is still unasked: **does the menu's designer still have the source file?**
3. **The terrace overlay paint-out**, if `ig-02` is used prominently.
4. **Desserts**, if the design wants the four homemade cakes shown rather than listed.

**No images were commissioned at this stage.** Item 1's test files are kept only so `/ewf:media`
does not repeat the experiment; the design stage decides what it actually wants first.
