# Design critique — Sa Pamboleria moodboard directions

Target: `.studio/moodboard/directions.html` · 2026-09-20
Rubric: `guidelines/aesthetics.md` (verbatim checklist + substance rules 11–16), `motion.md`, `copy.md`
Binding docs: `.studio/brief.md`, `.studio/client.json`. No `DESIGN.md` exists yet, so the brief governs.
Evidence: `shot-desktop.png` / `shot-mobile.png` in `.studio/qa/critic/moodboard-directions/`, the HTML source,
WCAG maths on the declared hex values, `menu.json`, `social-image-index.json`, and pixel sampling of
`refs/casteuler/shot-desktop.png`.

Judged as three designs. The presentation surface (system-ui, grey) is not judged.

---

## Verdicts

| | Direction | Verdict |
|---|---|---|
| 1 | `ember-brasa-premium` | **BLOCK** |
| 2 | `navy-menu-typographic` | **BLOCK** |
| 3 | `olive-terrace-daylight` | **BLOCK** |

None is unsalvageable. D3 is closest — its fails are local. D2's is structural.

---

## Registry — independently verified

`registry.mjs check` run per direction against the **declared dominant** (page background), sector `restaurant`:

- Newsreader / `#3A1418` / ember-brasa-premium → `{"checked":7,"flags":[],"clear":true}`
- Bricolage Grotesque / `#2E4162` / navy-menu-typographic → `{"checked":7,"flags":[],"clear":true}`
- Fraunces / `#E8DCC4` / olive-terrace-daylight → `{"checked":7,"flags":[],"clear":true}`

**Clear, confirmed — the page's claim is true.** No typeface is on the ban list or among the 7 entries
(Roboto, Space Grotesk, Brillante/Editorial Today, Grift, Schibsted Grotesk/Instrument Serif, Archivo ×2).

One adjacency the tool cannot see: `panespatagonia` (food-supplier, added 2026-09-19) carries navy
`#1B365D` as its **accent**. D2's **dominant** `#2E4162` is RGB distance **22.5** from it. The checker only
compares dominant-to-dominant, so it does not flag; a navy-led food client one day after a navy-accented
food client is still worth the owner knowing.

---

## Cross-cutting — applies to all three

1. **Three directions, one ending.** All three close with *Què diuen* (review quotes, no media) then
   *Trobar-nos* (map, hours, tap-to-call, week strip). D1 and D3 use the identical week-strip-with-today-lit
   device. The last two sections of the page were not designed three times; they were designed once and
   pasted. Rule 12 (attention after the hero) and rule 11 (device not liftable).
2. **A live "open now" state on hours the brief calls blocking.** All three storyboards promise a live
   open-now / current-band state. `brief.md` GAPS: *"Opening hours — Google and TripAdvisor disagree on
   closing days and times. Wrong restaurant hours cause real harm."* No direction carries a `[CONFIRM:]`
   on it. Rule 14 / copy.md rule 3.
3. **The family is missing from all three.** The brief's identity line is *"Warm, unpretentious, family-run"*
   and the voice traits are *"warm · unpretentious · generous · local-first"*. No direction has a section
   about the people. The reason is visible in the brief (*"no founding date, owner names or origin story, so
   'about' has nothing factual to stand on"*) — which is **exactly** the case rule 14 forbids:
   *"A missing fact is not a reason to delete a section."* Three `[CONFIRM: family name / years open /
   who is on the grill]` lines would have carried it. **FAIL, all three.**
4. **No direction states files used vs. available.** Checklist line: *"Asset pack used broadly — state files
   used vs. available and justify the gap."* Counted from the media lists against 22 usable files
   (`social-image-index.json`): **D1 8/22, D2 10/22, D3 11/22.** 11 of 17 catalogued `product` shots
   (ig-03…ig-08, ig-13, ig-16, ig-22 and others) appear in none of the three.
5. **The same near-identical pair in all three.** `ig-14` ("Charcuterie board with cured meats, cheese,
   peppers, bread slices on wood") and `ig-19` ("Close-up of charcuterie with cured meats, cheese, bread,
   olives") are listed **together** in D1, D2 and D3. Rule 13: *"never run two images of the same subject or
   composition."* **FAIL, all three.**
6. **People / video.** No usable people photo exists (`ig-18` is the only one and is flagged
   `identifiable_person, heavy_text_overlay, video_cover`), so rule 13's "people appear" does not fire.
   `client.json.social.other` is `[]` and the only video cover is unusable — so "video considered" is
   effectively satisfied by the research, but no direction says so out loud.
7. **The same headline trick in all three specimens.** See per-direction fails. `.specimen .accent { color:
   var(--d-accent) }` with `<h3>Carns a la <span class="accent">brasa</span></h3>`, `Pa amb <span>oli</span>`,
   `Sa <span>terrassa</span>`. Checklist, verbatim: *"No single word of a headline picked out in
   italic/bold/colour as a trick."* Visible in `shot-desktop.png` at each specimen. **FAIL ×3.**
8. **Banned copy phrases:** grep of the full source returns nothing from `copy.md`'s list. PASS.

---

# Direction 1 · Sa Brasa (`ember-brasa-premium`) — BLOCK

### Checklist

**Layout** — PASS. Not the hero/three-cards/testimonials stack; 7 sections with differing rhythm
(full-bleed band, vertical ladder, draggable strip, overlay). No identical rounded cards.
Hero is cut-out + headline + price line, not headline/number/label/gradient.
*Caution:* hero sketch reads "script logo, small, **centred**" and the headline centred under the cut-out —
the composition as sketched is symmetrical throughout. Alignment is not yet a decision.

**Type** — **FAIL** (one line). Newsreader/Hanken Grotesk: not banned, not in the registry, and the
evidence is the strongest of the three (Etxebarri Canela 67px/100 over Untitled Sans 17px, measured).
Fails: *single word of the headline picked out in colour* — "**brasa**" in ember `#E0642C`.
*Caution:* `13 cuts · €12–24 → opens la carta` puts the banned trailing `→` on the hero's only CTA, and
`INCA · MALLORCA` is a tracked-out ALL-CAPS eyebrow (`letter-spacing:.14em; text-transform:uppercase`) —
the exact move `board.md` condemns in Cas Teuler.

**Colour and surface** — **FAIL** (quality floor). Three of the four stated ratios verify exactly
(salt/oxblood 13.56:1, ember/oxblood 4.66:1, salt/char 16.23:1 — recomputed, all correct).
But the fifth swatch, **Aged `#8E4C56`, role "rules, hover"**, measures **2.57:1 on oxblood `#3A1418`**.
That is under the 3:1 floor for non-text UI and graphical objects, and far under 4.5:1 if "hover" is a text
state. It is the one swatch the direction's own contrast note omits. Not a tinted near-black stand-in —
the derivation from the dry-aged beef is honest — but the palette ships a failing role.

**Content and detail** — **FAIL**. `ig-14`, `ig-19` are listed as "berenar **and desserts**" but
(a) they are near-identical charcuterie boards, and (b) **the storyboard has no berenar section and no
dessert section** — the two files have nowhere to go. Meanwhile the brief lists *"four homemade cakes
€6.50"* praised by reviewers, and no dessert photograph exists anywhere in the 22.

**Motion** — PASS with a caution. "The plating" (cut-out settles, salt flakes land staggered) is one
signature moment, expresses the subject, load-only, reduced-motion final state stated. That is right.
*Caution:* the storyboard also gives the hero *"Cut-out tilts a degree with pointer"* — a second,
continuous, non-triggered motion. motion.md rule 2. It is also the ornament rule 8 asks you to remove.

**Substance** — **FAIL ×3**.
- *El lloc* — device: "Facts as icon + label + one line over the duotoned terrace". That is lifted verbatim
  from Etxebarri (board.md: *"Icon + label + short paragraph pairs in two columns"*) and would drop into any
  restaurant on the island unchanged. Not a device. **Rule 11 FAIL.**
- *Què diuen* — device: "review quotes set large; the number once, enormous". No media, no mechanism; it is
  a heading and some big type. Liftable. **Rule 11 FAIL.** It also brushes the banned hero pattern
  (one big number + small label) one section from the bottom.
- Media breadth 8/22, unstated, with a near-identical pair inside it. **Rule 13 FAIL.**
- *Good:* **the cut ladder** (13 cuts as a ruled vertical price ladder like a butcher's board, row opens to
  its photo and weight) is a real, client-specific device and the best single idea in the whole set.

### The Cas Teuler question — tested, not accepted

Measured from `refs/casteuler/shot-desktop.png` (pixel histogram + reading the page):

- **Board.md's premise is wrong.** It says Cas Teuler "owns dark-and-fiery". The page is **38.3% pure white**;
  its brand colour `#893529` (brick red-brown) covers 7.7% as header/footer bars and copper `#CEA26F` 1.4%.
  It is a **white page with dark photography**, not a dark page.
- **Axis 1 ("oxblood rather than copper-and-flame") — holds, for the wrong reason.** D1's ember `#E0642C` is
  distance 93 from their copper `#CEA26F`; D1's aged `#8E4C56` is distance 51 from their `#893529`. D1's dark
  oxblood *field* is further from them than the board realised, because their field is white.
- **Axis 2 ("plateless cut-outs rather than plated-on-wood") — holds.** Their nine-up gallery is entirely
  plated-on-board/slate; no cut-outs anywhere.
- **Axis 3 ("a real type scale rather than a 20px h1") — holds.** Uncontested.
- **The adjacency the board never named.** Cas Teuler's hero caption box reads **"CARNES A LA BRASA"**.
  D1's specimen headline is **"Carns a la brasa"** — the same three words, translated, over a dark red-brown
  field, beside dark meat photography. The three axes differentiate the *treatment*; nothing differentiates
  the *proposition*. D1 leads with the one thing the competitor already owns the search result for, while the
  client's own name and the ground the competitor cannot stand on — pa amb oli, the terrace — are sections 3
  and 5. That is the real risk, and the risk box does not mention it.

### Conflict with the brief

The brief records, dated and explicit: *"**Decided 2026-09-20:** the hero is a full-bleed crop of `ig-12`
(alternate `ig-14`) — the honest free route… The cut-out treatment stays available if a shoot or paid
generation is funded later."* D1's hero is the cut-out, and of `ig-11`, not `ig-12`. The board's €0.0024
Magnific test is fair grounds to **reopen** that decision — but D1 presents the reversal silently. An owner
reading directions.html cannot see that a recorded decision is being overturned, or that the mask
*"still has fragments to clean up"* (board.md).

### What to change (3)

1. **Recolour the headline.** Set "Carns a la brasa" in one colour at one weight (`.specimen h3` /
   `<span class="accent">`). Spend the ember on the cut ladder's active row instead — one accent, one job.
2. **Replace *El lloc* and *Què diuen* with devices.** The icon+label grid is Etxebarri's; the big-quote block
   is nobody's. The client has two terraces, free parking and an 8:30 *berenar* — and 11 unused product
   photographs. Conflicts with substance rules 11 and 12, and with the brief's *"Deep local following"*,
   which deserves better than a number set large.
3. **Fix `#8E4C56` and declare the hero reversal.** Either lighten the "rules, hover" swatch to ≥3:1 on
   oxblood (≥4.5:1 if it ever carries text) or give the role to ember. And put one line in the risk box
   saying the cut-out hero overturns the brief's 2026-09-20 decision, on the strength of the Magnific test,
   with the mask cleanup still outstanding.

---

# Direction 2 · La Carta (`navy-menu-typographic`) — BLOCK

### Checklist

**Layout** — PASS with a caution. Seven sections, real variation (keyline frame, menu column, clock strip,
one bleed-out). *Caution:* the hero is fully symmetrical — wordmark "large, **centred** on navy", index lines
below, frame around everything. Defensible as a menu cover, but the page then has no asymmetry until
*La terrassa*.

**Type** — **FAIL** (one line). Bricolage Grotesque / Source Serif 4: neither banned nor in the registry.
Fails: *single word picked out in colour* — "**oli**" in `#E4B33F`.
*Caution on the evidence:* the stated argument is Tacos My Guey (one display face at 74px) + Da Maria
(a **slab** serif, Bitter, for body). Bricolage is not a condensed cap face like Bebas Neue Pro and Source
Serif 4 is not a slab. The measured work supports the **roles**, not these two faces. Rule 3 asks for the
published work the choice comes from; what is offered is an analogy. Bricolage is also the most
of-the-moment variable grotesque on Google Fonts right now — no registry flag, but it will date.

**Colour and surface** — **FAIL** (quality floor). The navy is the best colour decision in the set: it is the
client's **own ink**, recovered by white-balancing the menu photograph. The three stated ratios verify exactly
(paper/navy 9.16:1, oli/navy 5.28:1, navy/paper 9.16:1 — recomputed, all correct).
But the palette assigns **Tomàquet `#C8382B`** the role **"sparingly, prices"** — body-size text — and
`#C8382B` on `#2E4162` is **1.98:1**. Unreadable, and absent from the direction's own contrast note.
(Olivera `#8FA37A` on navy is 3.75:1 — fine as "illustration only", but it is one role change from failing too.)

**Content and detail** — **FAIL ×2**.
- The hero index prints **"Per picar 9"**. `menu.json`'s `para-picar` section has **11 items**
  (11 + 13 + 13 + 3 + 4 + 6 + 3 + 4 = 57). The one number the whole hero device rests on is wrong.
  copy.md: *"Confirm every number, name and claim traces to brief.md/profile.json."*
- The hero sign-off is **"Inca · des de sempre"**. The brief: *"no founding date, owner names or origin
  story."* "Since forever" is an invented claim about longevity in the client's largest piece of type.
  copy.md rule 3 — never invent facts.

**Motion** — PASS with a build correction. "The frame draws" is one moment, on load, reduced-motion state
stated. It expresses the idea. *But the demo animates the banned properties:*
`@keyframes drawX { to { width: calc(100% - 16px) } }` / `drawY { to { height: … } }`.
motion.md: *"Animate transform and opacity only. No animating top/left/width/height/margin."*
D1 says "the build uses GSAP with `matchMedia`"; D2 says nothing, so the CSS stands as the spec. Respecify
as `scaleX`/`scaleY` from a transform origin.

**Substance** — **FAIL ×2**.
- **The menu is said three times.** *Hero* = the 8 sections as a typographic index; *A la brasa* = "set as a
  real menu column: Source Serif names, leader dots, prices right-aligned"; *La carta* = the full menu as an
  overlay card. Rule 15: *"No section repeats what another already said."* The brasa column and the overlay
  are the same artefact at two sizes. Three of seven sections are menu-as-typography — which is the thesis,
  but the thesis has to change what the visitor knows each time, and here it does not.
- Media breadth 10/22, unstated, with the `ig-14`/`ig-19` pair.
- *Good:* **"One bread, thirteen toppings"** (fixed bread base, choosing a topping swaps photo and price) and
  **the clock strip** (berenar / dinar / sopar) are both genuinely this client's, and the clock strip is the
  only place in any direction where the 8:30 *berenar* gets a section of its own. *Feasibility:* the topping
  device implies 13 states; the pack has 4 pa amb oli files (`ig-10`, `ig-12`, `ig-20`, `ig-30`).

### Is the photograph-free hero a real idea or an evasion?

**Both, and as written it lands on evasion.** The idea is real: the client's only brand artefact *is* a
printed menu, the wordmark is the only identity that exists, and an 8-section index with counts is genuine
navigation rather than decoration — that is a better reason to drop the photograph than most sites have.

It fails on three concrete things:

1. **It contradicts a stated owner must-have.** `brief.md` Practical: *"Owner must-haves: menu restyled in an
   in-page overlay, a transparent logo from the menu photo, **a product-showcase hero**."* `client.json`:
   *"Hero idea (owner): a professional photograph of a pa amb oli… product-showcase treatment."* D2's hero
   has no photograph at all. A direction may argue against a must-have — it may not quietly ignore it. The
   pitch instead claims D2 is *"built… around the one thing the brief calls a must-have"*, naming the overlay
   and passing over the hero.
2. **It replaces the photograph with an asset that does not exist.** `brief.md` **Blocking**: *"Logo —
   printed inside a photo only."* The media list concedes it: *"`logo-extracted.png` — wordmark, **to be
   traced to vector at media stage**."* The reference image in the page is visibly a noisy crop on
   blue-cast paper with a vegetable in the frame, ~350–400px wide per `asset-index.json`. The boldest move in
   the set makes the single most fragile asset the largest object on the page.
3. **It never says why.** The honest sentence — *"the photography is flat-lit and edge-cropped, so this
   direction declines to open on it"* — appears nowhere. Without it, the reader cannot tell conviction from
   avoidance. State it and the idea gets much stronger.

*One measured note on the keyline:* Cas Teuler's hero already sets its caption inside a thin gold keyline box
(`refs/casteuler/shot-desktop.png`, hero region). D2's frame is a different move (it frames the whole page,
from Da Maria) but the claim *"lift it into another restaurant's site and it stops meaning anything"* is
overstated — the nearest competitor is already using a thin gold rule as a framing device.

### What to change (3)

1. **Put a photograph in the hero, or argue on the record.** Either let the menu card sit over one
   full-bleed plate inside the keyline, or add an explicit paragraph saying the direction declines the
   owner's product-showcase hero and why. Conflicts with `brief.md` Practical → *Owner must-haves*.
2. **Fix the two facts in the largest type on the page.** `Per picar 9` → **11** (from `menu.json`), and cut
   `des de sempre` or replace it with `[CONFIRM: any dels inicis]`. Conflicts with copy.md rule 3 and with
   the brief's GAPS, which say there is no founding date.
3. **Collapse the duplicate menu, and fix `#C8382B`.** *A la brasa* should do something the overlay cannot —
   weights, ageing, what "madurada" means, the `ig-09` slate — not repeat the overlay in column form. And
   prices at 1.98:1 on navy must move to Oli `#E4B33F` (5.28:1) or to the paper card.

---

# Direction 3 · Sa Terrassa (`olive-terrace-daylight`) — BLOCK

### Checklist

**Layout** — PASS. Best alignment decision in the set: wordmark small **left**, matted photograph, headline
breaking the mat — a real grid-break, and the only one of the three heroes that is not centred. Sections
vary (mat → hotspot photograph → letterpress list → one full-bleed dark band → overlay → margin quotes).

**Type** — **FAIL** (one line). Fraunces / Karla: neither banned nor in the registry, and the Da Maria
Playfair-at-244.8px reasoning is sound. Fails: *single word picked out in colour* — "**terrassa**" in
olive `#4E5C28`.

**Colour and surface** — **FAIL** (quality floor). Two of the three stated ratios verify exactly
(ombra/grava 10.66:1, olivera/grava 5.36:1). The third, *"paper on olivera 5.87:1"*, **matches no colour in
D3's own five-swatch palette** — there is no "paper" swatch; grava on olivera is 5.36:1 and `#F5F2EA` on
olivera is 6.51:1. A figure presented as measured that traces to nothing.
Worse, the *Tretze* section specifies a **"letterpress list in Fraunces, oat on oat"** — tone-on-tone text —
and the contrast note does not cover it. The only oat-on-oat pair in the palette (grava `#E8DCC4` on fusta
`#735F41`) is **4.49:1**, i.e. under AA at body size before any "letterpress" softening.
*Credit where due:* this is **not** the cream/serif/terracotta default — the accent is a measured olive from
the client's own planting, and `#E8DCC4` is distance 54–65 from the three cream dominants in the registry.
The choice is argued, not defaulted.

**Content and detail** — **FAIL**. The hero line reads
`Obert avui · 8:30 berenars · aparcament gratuït` — the banned `A · B · C` meta string, and a reflex
three-item list (copy.md structural tics). It is also the live-hours claim from cross-cutting point 2,
placed in the hero, on hours the brief calls blocking.

**Motion** — PASS with a caution. "Light through the thatch" is one load moment, under three seconds, never
repeats, expresses the place. *Caution:* the reduced-motion fallback is
`.light-demo::after { transform:none; opacity:.35 }` — a **permanent warm gradient layer over the hero
photograph** for reduced-motion users. Checklist: *"No gradient washes as decoration."* The reduced-motion
state should drop the layer, not park it. Also: a full-width gradient sweeping a hero image is the
"large filtered layer" motion.md warns about on phones.

**Substance** — **FAIL ×2**.
- **`ig-02` carries the hero *and* the whole second section.** Hero: *"Put the visitor on the terrace before
  anything else"* (`ig-02`). *Sota els para-sols*: *"What it is actually like to eat there"* (`ig-02`).
  The same single photograph, twice, in consecutive sections — and `board.md` states *"it is the only usable
  terrace shot."* Rule 13 (*no two near-identical images*) and rule 15 (*say each thing once*): the second
  section adds hotspot labels to the picture the visitor has just looked at. Hotspots on a 1080px phone
  photograph at desktop width will also not hold up.
- *Què diuen* — "pull quotes set into the wide oat margin, Fraunces 300", static, no media. Same non-device
  as D1's. **Rule 11 FAIL.**
- Media breadth 11/22 — the widest of the three, and the only one to reach for `ig-15`/`ig-17` (fish) and
  `ig-29` (oxtail) — but the ratio is still unstated, and `ig-12`/`ig-14`/`ig-19` are grouped as
  "the abundance customers praise", which is three near-identical spreads in one row.
- *Good:* **the one dark band** (`ig-09` aged beef on slate, reversed out of the page, 13 cuts over slate) is
  the best use of the sharpest file in the pack and the clearest "spend boldness in one place" in the set.

### The hero's hidden cost

`images/terrace.jpg` (= `ig-02`) has the client's **script wordmark baked in as a large white overlay across
the centre of the frame**, plus promo text — visible in the direction's own motion demo in
`shot-desktop.png`. `social-image-index.json` flags it `baked_in_text_overlay`; `board.md` notes
*"the logo is baked into this image as an overlay."* D3 also places the navy script wordmark top-left, so as
drawn the hero shows the logo twice. *"Promo text to be cleaned at media stage"* understates a retouch across
tables, parasols and ceiling on a 1080px source. `fb-01` is flagged `duplicate_of_ig-02` and carries the same
overlay, so it is not an escape route.

### What to change (3)

1. **Give *Sota els para-sols* its own image, or fold it into the hero.** Using the only terrace photograph
   twice in a row is the direction's weakest moment and it sits in position two. Conflicts with substance
   rules 13 and 15 and with the direction's own thesis (*"the one thing the competitor has no photograph
   of"* — shown twice does not make it two things).
2. **Measure the oat-on-oat list, and fix the phantom 5.87:1.** Name the two hexes for the *Tretze*
   letterpress treatment and state the ratio; at body size it needs ≥4.5:1, and the palette's only oat-on-oat
   pair is 4.49:1. Quality floor, non-negotiable per rule 10.
3. **Rewrite the hero's third line.** `Obert avui · 8:30 berenars · aparcament gratuït` → one sentence in the
   client's own voice (the brief's voice samples are exclamatory and warm, e.g. *"Nuestra terraza lista para
   vosotr@s"*), with `[CONFIRM: 8:30 berenar still running]` attached. Conflicts with the copy.md banned
   `A · B · C` string and with the brief's blocking hours gap.

---

## If one has to go forward

**D3** is nearest to shippable: every fail is local and cheap (one span recolour, one hero line, one image
swap, one contrast measurement, one device for the quotes), it needs no cut-out and no generated asset, and
it stands on the ground the competitor cannot reach.

**D1** owns the best single device in the set (the cut ladder) and the strongest type evidence, but it leads
with the competitor's own headline and must declare its reversal of the brief's hero decision.

**D2** has the best colour argument of the three — it is the only direction using a colour the client
actually owns — and the worst structural problem: a hero that drops an owner must-have in favour of an asset
that does not exist yet, with a wrong number and an invented claim set in the largest type on the page.

Whichever proceeds, all three cross-cutting items (the pasted ending, the unconfirmed live hours, the missing
family section, the unstated asset ratio) have to be fixed before `DESIGN.md` is written.

---
---

# Re-review — pass 2 (revised directions)

Re-captured to `.studio/qa/critic/moodboard-directions-rev2/`. Every fix re-verified from source, CSS and
recomputed WCAG maths; registry re-run; `board.md` correction confirmed applied.

## Re-verdicts

| | Direction | Pass 1 | Pass 2 |
|---|---|---|---|
| 1 | `ember-brasa-premium` | BLOCK | **BLOCK** (2 narrow fails, both new) |
| 2 | `navy-menu-typographic` | BLOCK | **REVISE** (1 fail) |
| 3 | `olive-terrace-daylight` | BLOCK | **BLOCK** (2 fails, one substantive) |

**This reverses my pass-1 ranking.** D2 — the one I called structurally broken — made the most complete
repair and introduced the fewest new defects. D3, which I called nearest to shippable, introduced a false
measured ratio and an invented artefact. The evidence moved; so does the ranking.

## Verified fixed (re-measured, not taken on trust)

- Accent word removed from all three headlines: `grep -c 'class="accent"'` → **0**. Confirmed rendered in
  `rev2/shot-desktop.png`. The accent is now a `border-bottom:1px solid var(--d-accent)` rule under the eyebrow.
- **D1** aged `#A8636C` on `#3A1418` = **3.61:1** — claim exact; role correctly restricted to non-text.
- **D2** oli `#E4B33F` on navy = **5.28:1**, tomàquet `#C8382B` on paper = **4.63:1** — both exact, and the
  1.98:1 navy figure is now printed as the reason for the restriction. Good practice.
- **D3** fusta `#63512F` on grava = **5.63:1** — exact, with the `#735F41` → `#63512F` darkening and its
  4.49:1 origin explained. The phantom "paper on olivera 5.87" is gone.
- **D2** counts: hero prints `Per picar 11 · Pa amb oli 13 · A la brasa 13 · Ensalades 3 · Peix 4 ·
  Especialitats 6 · Per a nens 3 · Postres 4` — matches `menu.json` section-for-section, sums to 57. ✔
- **D2** motion rebuilt: `transform:scaleX(0)` + `transform-origin` + `@keyframes growX { to
  { transform:scaleX(1) } }`. No width/height animation remains anywhere in the stylesheet. ✔
- **D3** reduced motion: `.light-demo i { display:none }` — layer removed, not parked. ✔
- Asset ratios stated **and arithmetically correct**: D1 12 used + 10 unused = 22; D2 13 + 9 = 22;
  D3 14 + 8 = 22. `ig-19` dropped from all three. Absence of any dessert photograph stated in all three.
- `[CONFIRM: hours]` present on every live-hours state; `La família` present in all three with
  `[CONFIRM: owner names, founding year]`.
- **Endings genuinely differentiated** — three distinct reviews devices and three distinct closing devices;
  the shared week strip now appears in D1 only.
- `board.md` correction applied accurately and attributed to sampling, including the "CARNES A LA BRASA"
  shared-proposition point.
- Registry re-run post-revision: all three `{"checked":7,"flags":[],"clear":true}`.

## The two things I was asked to test rather than trust

**1. D1's `El lloc` and `Què diuen` — devices, or relabelled?**

- `El lloc` → **"the parking approach"**: *"the terrace shot annotated with… where to leave the car, which
  terrace is covered, whether you can just turn up."* **No longer Etxebarri's** icon+label grid, and it is
  now anchored in a real, repeatedly-praised fact (*"Un lloc on és fàcil aparcar"*). But compare D3's hero:
  *"Matted photograph with annotations in the mat — parking, which terrace is covered, the berenar tables."*
  **The two directions now share one device on one photograph with the same three facts.** D1 traded a
  device borrowed from a reference for a device borrowed from its sibling. Not a checklist fail — it is
  client-specific now — but the distinctness table does not test a "place device" axis, so it does not catch it.
- `Què diuen` → **"4,3"**: half-fixed, honestly. *"the Catalan quotes hung off the same ladder the cuts use"*
  is real design thinking — a motif carried across two sections, and it cannot be lifted without bringing the
  ladder, so it clears rule 11. But the headline idea, *"the score set as one enormous numeral, the 4.3/5
  drawn as a filled ember rule beneath it"*, is a rating bar: the single most generic review treatment on the
  web, and close to the banned "big number + small label". The connective tissue passes; the idea underneath
  it is still the weakest in the direction.

**2. D2's maturation scale — does it avoid rule 15 or move it?**

**It avoids it.** The three menu moments now carry three different payloads: the hero index gives *section
names and counts* (how big the menu is), `A la brasa` gives *cuts on a dry-ageing timeline with no prices*
(how the meat is made), the overlay gives *all 57 dishes with prices* (the carta). Each changes what the
visitor knows. `"Prices live in the overlay, not here, so the menu is not set twice"` is an accurate
description of what the storyboard now does, and the ageing content does not exist in the printed menu at
all — so it is additive, not duplicative.

**One contingency, flagged not failed:** the section's entire payload is ageing days that do not exist.
`brief.md`: *"the bio's dry-aged 'Carnes Maduradas Premium' isn't on [the menu]. → Owner confirms."*
It is correctly carried as `[CONFIRM: ageing days per cut]` — rule 14 handled properly. But a family
restaurant may simply not track days per cut. If that answer comes back empty, the section collapses to a
list of 13 cut names and **the rule-15 repetition returns**. A fallback needs to exist before build.

## New and wrong — introduced by this revision

1. **D3: a false measured ratio, under the words "Every swatch, measured."** The palette note claims
   *"navy on grava **7.94:1**"*. `#2E4162` on `#E8DCC4` is **7.5491:1**. Both pass AA, so no quality-floor
   breach — but this is the same defect class as the "paper on olivera 5.87" that was just corrected, in the
   same paragraph, in the direction that was told about it. **FAIL** (copy.md: confirm every number).
2. **D3: `Taula per taula` rests on an artefact nobody has.** Device: *"Quotes anchored to a **line plan of
   the two terraces** — each review pinned to where it would have been said."* There is no floor plan, no
   table layout, and one usable terrace photograph. The plan would be drawn from nothing, and real reviews
   would be pinned to invented positions. Every other unknown on this page carries a `[CONFIRM: …]`; this
   one — in D3's best device — carries none. **FAIL** (rule 9: no invented content; rule 14's own remedy
   unapplied).
3. **D1: the eyebrow is now a banned `A · B · C` meta string.** `<p class="eyebrow">Inca · Mallorca · des de
   la graella</p>` — was two items, revised to three. Visible in `rev2/shot-desktop.png`. This is the exact
   line D3's hero was failed on last round. **FAIL.**
   *(D2's `Terrassa · Pa amb oli · Carns a la brasa` is exempt and stays exempt: it is the client's actual
   printed logo lockup, voice sample 2 — a real artefact, not a styling tic.)*
4. **The banned `→` now sits in two heroes, not one.** D1 `13 cuts · €12–24 → opens la carta` (carried over,
   never addressed) and D2 `"Obert avui" + tonight's hours → opens la carta` (**new**). Both are the hero's
   only CTA, so every CTA shown carries the arrow. Same checklist line as item 3. **FAIL** for both directions.
5. **D1: `La família` is only a heading + paragraph + button.** Device *"A char card: who cooks, and the
   phone as the only way to reach them"*, media **None**, interaction tap-to-call. The section I asked for was
   added as a card with no device and no image, in the one direction where it carries no media at all
   (D3 gives it `ig-12`; D2 folds it into the colophon with the map). **FAIL** — checklist:
   *"No section is only a heading + paragraph (+ button)."*
6. **D1: `Berenars` is thin.** *"A two-item price card set into the margin beside the charcuterie shot."*
   Compare D2's clock strip on the same content. It also prints berenar prices that `brief.md` lists as
   **low confidence** (*"€10 berenar (one undated aggregator)"*); the `[CONFIRM:]` covers whether the service
   runs, not what it costs. Not a fail — it has media and a place — but it is the weakest new section in the set.
7. **D2: the hero's live-hours line carries no `[CONFIRM:]` at the point of use.** The confirm sits in the
   Colophon row instead. D1 and D3 mark it where it appears. Minor inconsistency in an otherwise thorough pass.

## Carried, unaddressed from pass 1 (not re-counted as fails)

- **D1** hero still specifies *"Cut-out tilts a degree with pointer"* — a second, continuous, non-triggered
  motion beside the signature moment (`motion.md` rule 2), and still the obvious ornament for rule 8.
- **D1** hero composition still centred throughout (*"script logo, small, centred"*); alignment is still not
  a decision in this direction. D3 remains the only one that decides.
- **D2** `Tretze` still implies 13 topping states against 4 available pa amb oli files.
- **D1's** hero reversal is declared on the page, which is what I asked for — but `brief.md` is **unmodified**
  (git: only `.studio/status.json` is dirty) and still records *"Decided 2026-09-20: the hero is a full-bleed
  crop of `ig-12`, not the cut-out."* The binding document and the direction still disagree. I cannot verify
  the owner's in-session reversal from anything on disk; it is a documented assumption, not evidence.
  Reconcile `brief.md` before `DESIGN.md`.

## On D2's photo-free hero — resolved by disclosure

The pass-1 BLOCK was not that D2 declines the owner's hero; it was that it declined it **silently** while
claiming to serve the brief. The risk box now states the contradiction outright, argues both sides, concedes
*"it is also the convenient move"*, names the cost (*"makes the weakest asset in the pack… the largest object
on the page"*), and points the owner to D1 for their own idea. That is the honest version, and it is what a
moodboard is for. **No longer a fail.** If D2 is chosen, record the owner's sign-off on dropping their stated
product-showcase must-have before `DESIGN.md` is written.

## What to change

**D1 (2 fails — both cosmetic, ~15 minutes)**
1. Eyebrow back to two items or a phrase: `Inca · Mallorca · des de la graella` → `Des de la graella, a Inca`.
2. Drop the `→` from `13 cuts · €12–24 → opens la carta`.
3. Give `La família` a device and an image, or fold it into `Trobar-nos` as D2 does with its colophon —
   a section added to satisfy a critic and left as a card is rule 12's failure mode, not its fix.

**D2 (1 fail — ~2 minutes)**
1. Drop the `→` from the hero line, and move `[CONFIRM: hours]` up to it.
2. Before build: a fallback for `A la brasa` if the ageing days come back unknown.

**D3 (2 fails)**
1. `navy on grava` is **7.55:1**, not 7.94. Correct it — the credibility of "every swatch, measured" is the
   whole point of that block.
2. `Taula per taula` needs `[CONFIRM: terrace layout / table plan]`, or the device has to work from the one
   photograph rather than an invented plan.

## Standing recommendation, updated

**D2** is now the closest to ready: one arrow to delete, and it is the only direction built on a colour the
client owns, the only one with all 57 dish counts verified against source, and its rule-15 problem is
genuinely solved rather than moved. **D3** remains the safest against the asset pack but has just shown the
failure mode it was corrected for. **D1** delivers the owner's hero idea and owns the best single device in
the set (the cut ladder), but still opens with the competitor's own sentence, and its brief reconciliation
is outstanding.
