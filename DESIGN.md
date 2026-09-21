# DESIGN: Sa Pamboleria

**Aesthetic:** _decided at the design stage_
**In one line:** a family restaurant in Inca that people already trust locally should feel, in five seconds, like somewhere generous and unpretentious you could turn up at tonight without booking.
**Sector:** restaurant  ·  **Languages:** ca, es, en  ·  **Chosen:** 2026-09-21, admin

## What this site must do

They have **no website at all** — two dead domains (`Sapamboleria.com`, `sapamboleria.es`) are
still advertised on Facebook. Everything below is a job the current absence of a site fails.

1. **Show the menu, restyled, in the visitor's own language.** The must-have. 8 sections,
   57 dishes with prices, transcribed in `.studio/sources/menu.json`. It opens **in-page as an
   overlay**, not as a separate page — the site is one page. The printed menu is Spanish-only;
   ca and en are translations and the owner should check the Catalan.
2. **Make the food look worth the trip**, using photographs that are honest phone shots.
3. **Show the terrace** — covered, thatched, with free parking. It is the single most
   distinctive thing they own and no competitor has an equivalent.
4. **Get the phone to ring.** There is **no email and no booking system**. The phone number
   (+34 971 67 79 75) is the only conversion, and it must be tap-to-call on mobile.
5. **Answer the arrival questions**: where to park, when they are open, whether you can just
   turn up. You can — say so.
6. **Pick the starting language from the device** (ca/es/en) with a manual switcher. Not a
   hardcoded default.

## Visitor

- **Who:** mostly locals from Inca and the surrounding towns who already know the place or have
  heard it named — they write their Google reviews in Catalan. Secondarily, people staying in
  Mallorca looking for somewhere unpretentious that is not on the tourist strip. Families, and
  groups who want abundant food rather than a tasting menu.
- **Should feel, in five seconds:** that the food is generous and real, the place is relaxed and
  shaded, and that they would be welcome tonight. Their customers' own words are
  *"menjar abundant i gustós"* and *"el servei molt amable"* — that is the feeling to hit.
- **Should do:** phone, to check a table or ask about a group. Short of that: open the menu and
  read it to the end, or take the address. Opening the menu counts as success.

## Palette

_decided at the design stage_

Colour **evidence** from the client's own photographs, sampled from the pixels, is recorded in
`.studio/moodboard/board.md` — the recovered wordmark navy, the terrace's olive wood, gravel,
thatch and foliage, and the grill's slate and aged burgundy. It is evidence, not a palette.

## Typography

_decided at the design stage_

One constraint that does bind: **the client's wordmark is a brush script, and it is the only
real brand asset they own.** Nothing else on the page should be handwritten.

## Layout and spacing

_decided at the design stage_ — beyond the fixed facts that it is **one page** and that the menu
opens as an **in-page overlay**.

## Section storyboard

_decided at the design stage_

## Media plan

_decided at the design stage._ What exists: **22 usable images of 31 pulled**, all phone-shot at
1080px wide (1170 max), flat-lit, cropped hard to the frame edge. Indexed in
`.studio/sources/social-image-index.json`.

**Requested from client:**
- **The logo source file** — does the menu's designer still have it? Cheapest and best route to a
  vector wordmark, and **not yet asked**. Everything else means tracing a 447 × 350 px crop.
- **Confirmation of opening hours** — Google and TripAdvisor disagree on closing days *and* times,
  including whether the 8:30 *berenar* still runs. Blocking: wrong restaurant hours cause real harm.
- **Confirmation that the menu is current**, and prices. The photographed menu is undated and the
  Instagram bio's dry-aged "Carnes Maduradas Premium" does not appear on it.
- **Image rights.** Every photograph on this site comes from scraped social. The 2021 run was shot
  by a credited hired photographer (@alv_visuals). Assumed granted so design can proceed —
  **this does not unblock launch.**
- **Desserts and people**: no usable photograph of either exists. Four homemade cakes are on the
  menu with no picture; the one photograph with a person shows an identifiable customer.

## Imagery

_decided at the design stage_

## Signature motion

_decided at the design stage_

## Voice

Warm, unpretentious, family-run. Their own writing is short, exclamatory and emoji-led — an
invitation rather than a pitch; customers are generous and specific. Traits: **warm ·
unpretentious · generous · local-first · direct · proud of the produce.**

**The language split is the brand.** The logo is Catalan, the printed menu entirely Spanish,
Instagram Spanish, the Google reviews Catalan. Treat **Catalan as the brand's own voice** and
**Spanish as the operational one**. **Dish names stay Catalan in every language version.**

Real lines to draw on: *"Terrassa • Pa amb oli • Carns a la brasa"* (printed logo, ca) ·
*"Pa amb oli y Carnes Maduradas Premium"* (Instagram bio, es) · *"Menjar abundant i gustós i el
servei molt amable i pendent de nosaltres."* (Google, ca).

## Do

- Lead with **the bread and the terrace** — the two things the nearest competitor does not have.
- Use the customers' own Catalan where quotes are wanted; they are better than anything written.
- Say the practical things plainly: free parking, no booking needed, which terrace is covered.
- Treat the 13 pa amb oli and the 13 grill cuts as the substance of the site — that is the offer.
- Carry unresolved facts as `[CONFIRM: …]` rather than cutting the section around them.

## Don't

- **Don't invent an origin story.** There is no founding date, no owner names and no recorded
  history. If an "about" is wanted, it gets `[CONFIRM: …]`, not a plausible paragraph.
- **Don't publish opening hours** until the owner confirms them.
- **Don't publish the TripAdvisor rating.** A stale listing shows 2.6/5 from 11 reviews against
  **4.3 from 721** on Google. Google is the real figure; the owner should know the other exists.
- **Don't manufacture press.** There are no awards and no coverage — normal at this size.
- Don't correct the menu's own spellings silently ("De Baicon queso", "Hamburgesa Angus") —
  confirm them.
- Don't use the six Uber Eats reposts, the 320px avatar, or the frame showing an identifiable
  customer. They are excluded on quality and rights grounds independently of each other.

## Settled — raised in review, decided, do not re-raise

- **The hero.** Research recorded on 2026-09-20 that the hero would be a full-bleed crop of
  `ig-12`, *not* the owner's cut-out idea, because no pa amb oli shot had clean edges or
  resolution to spare. **The owner reversed this on 2026-09-20**, asking to enhance a source
  through Magnific and revive the product-showcase hero. **Reason:** it is the move all three of
  their own references share. Feasibility was then tested rather than assumed — see the image
  ideas in `board.md`. The cut-out is achievable as **food without its plate**; Magnific's
  background-removal endpoint returns **HTTP 403** on this API key, and there is **no Nano Banana
  tooling in this pipeline**, so no hand-reaching shot can be generated here today.

## Banned for this client

- Global: the anti-generic checklist (`guidelines/aesthetics.md`) and banned phrases (`guidelines/copy.md`)
- Registry: _checked at the design stage_, on the returned typeface, dominant colour and aesthetic.
- Client-specific: no second script typeface anywhere (the wordmark is the only handwritten
  element); nothing that reproduces **Cas Teuler**'s positioning — their hero already says
  "CARNES A LA BRASA", the same sentence as this client's own logo line, backed by studio fire
  photography this client cannot match.

## Registry entry (for `registry.mjs add` after approval)

_added by `design`, from what was actually designed — not from an intention._
