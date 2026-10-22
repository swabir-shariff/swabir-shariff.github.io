# List A — Wave 1: Content Edits (Oct 22, 2026)

Branch: `list-a-preview-oct22` · File edited: `index.html` only (plus two asset deletions).
Line numbers below refer to the **post-edit** `index.html`. No CSS tokens, type/spacing
system, breakpoints, motion JS, or `srcset` were touched — that is wave 2. The only JS
added is the A9 copy-button helper (see §6).

---

## 1. A7 — Copy pass (assume, don't argue)

| Section | Line(s) | Change |
|---|---|---|
| Hero | 526 | Sub-copy cut from three assertions to one claim: “I advise and speak where decisions get made — in boardrooms, at policy tables, and on conference stages.” |
| Accolades | 635–636 | H2 “A record that can be shown.” → “Honours and recognition.” Lede “every honour below is on the public record…” → neutral “From Scarborough to international recognition.” |
| Media | 845 | Kicker “Media & Public Record” → “Media”. |
| Whole page | 1013 | “public record” now appears exactly **once** — the footer line, unchanged. (Other two instances removed above.) |
| FAQ (visible) | 953 | Response-time answer rewritten: “Fast. If you're working to a deadline, name it in the enquiry and I'll match it where I can.” — “never an assistant or an inbox queue” cut. |
| FAQ (JSON-LD) | 470 | Same answer mirrored exactly in the FAQPage block. |
| FAQ | 929 | Lede trimmed to “The questions organizers and committees ask most.” (defensive tail “…answered the same way everything on this page is: straight.” cut). |
| Contact | 998 | Form-note sentence “Enquiries are answered personally.” cut. The contact lede (line 964) keeps “answered personally” as the single home of that promise — unchanged. |

## 2. A1 — Edit down

### 2a. Repetition audit — every appearance found, and what was done

**Scarborough Walk of Fame**
- Accolades card (kept — the one accolades claim), line 663.
- Hero “See me speak” video artefact (kept — media record, not a claim).
- Media coverage row “Scarborough Walk of Fame — Rising Star inductee” (kept — coverage record).
- Organizer bios, Media (kept — the brief mandates Walk of Fame Rising Star 2024 as a bio fact), lines 912/917.
- **CUT:** Selected Appearances engagements list line “Remarks — Scarborough Walk of Fame induction ceremony” — it merely re-claimed the honour; the induction is already on record via the accolades card, the hero video and the media row.

**Global News**
- Press strip (kept), line 573.
- Selected Appearances record “Interviewed on Global News, Dec 2021” (kept — appearance record), line 791.
- Media watch card + caption (kept — media artefact).
- **CUT (name-drop):** About prose (line 598) — “a Global News ‘Making a Difference’ feature in 2021 and a CP24 Tonight panel in 2022 among them” removed; sentence now reads “National media have turned to my voice on youth violence and community leadership.”

**CP24**
- Press strip (kept), line 574.
- Selected Appearances record “Panel guest on CP24 Tonight, Feb 2022” (kept — appearance record), line 790.
- Media watch card + caption (kept — media artefact).
- **CUT (name-drop):** same About prose edit as Global News above (one sentence covered both).

**Signature talk titles** (“Keys to the Whole House” / “Change the Starting Line” / “Every Piece of the Whole”)
- Signature Talks section (kept — the one home for the titles); each title now appears exactly once on the page.
- **CUT:** Services, Keynotes & Talks card (line 702) — the sentence listing all three titles replaced with “The keynotes are the three signature talks set out below.”
- FAQ “What formats can I book?” also referenced the signature talks — that Q&A was dropped in the FAQ trim (§2d), removing the repeat.
- Retained deliberately (not talk listings): the Philosophy section's prose (“keys to the whole house” / “every piece of the whole”, lower-case, naming the philosophy) and the hero positioning line (“Changing the starting line…”) — these are the philosophy/positioning statements, not title repeats.

**QECT in About prose** (line 597, “carried me to London as one of the QECT 100 Young Leaders”) — retained: QECT is outside the A1 enumeration, and the sentence is biographical narrative (the London trip), not a bare honour claim. Flagged here so wave 2 / Swabir can overrule.

### 2b. CTAs deleted (kept: nav “Enquiries”, hero CTA, contact enquiry panel)
- **DELETED:** standalone CTA band after Accolades (“Planning something for 2027? … Advisory & Speaking Enquiries”) — whole `.cta-band` block removed.
- **DELETED:** Services booking band (“Now accepting advisory and speaking engagements for 2027” + button) — whole `.booking-band` block removed.
- **DELETED:** enquiry button inside the Media downloads row (`.kit-band` “Advisory & Speaking Enquiries” button). The three download buttons in that row stay.

### 2c. Downloads
- Hero (line 531): link swapped from Media Kit → **Speaker One-Sheet only** (“Download the speaker one-sheet (PDF)” → `assets/Swabir-Shariff-Speaker-One-Sheet.pdf`).
- Contact (line 987): keeps Speaker One-Sheet; **Media Kit duplicate link removed**.
- Media downloads row (lines ~902–905): unchanged as the one archive — Media Kit + Speaker One-Sheet + Biography all stay there.

### 2d. FAQ trimmed 12 → 6 (visible section lines 930–956; JSON-LD mirrored exactly)
Kept: What are your fees? · How does booking work? · How far ahead should we book? (2027 availability) · Can we record or stream the talk? · What does an advisory engagement look like? · How quickly will we hear back? (answer rewritten, §1).
**Dropped questions (logged per brief):**
1. “What formats can I book?” — organizer-irrelevant once Services/Talks sections carry formats; also held a signature-talks repeat.
2. “Will you tailor the talk to our audience?” — covered by the scoping/proposal process in “How does booking work?”
3. “Where will you travel?” — travel terms belong in the written proposal.
4. “What do you need from us on the day?” — mic/clicker logistics; explicitly cut by the brief.
5. “Do you speak to schools and students?” — not booking-core for the advisor/speaker audience.
6. “Who do we contract with?” — contracting boundary already stated in the Contact form-note; not booking-core.
FAQPage JSON-LD (head, lines ~425–475) rebuilt to the same 6 Q&As; validated as parseable JSON and an exact text mirror of the visible FAQ.

## 3. A8 — Press strip (lines 573–577)
Honest typeset list kept (no logos). All five outlets now carry **identical markup**:
name + `<span class="press-ext" aria-hidden="true">↗</span>`. The marker was added to
Scarborough Mirror, CharityVillage and One Young World (Global News and CP24 already
had it). No new classes — `.press-ext` is the existing pattern.

## 4. A2 — Accolades rebuild (lines 637–676)
All five honours rebuilt as uniform typeset cards with the same structure:
`.yr` year → `h3` honour name → `.acc-body` awarding-body line → one-line citation
(→ verification link where one already existed: One Young World, Walk of Fame, CharityVillage).

- **QECT 2026** — the only card with an image: `assets/qect-award.webp` moved to a
  card-top `<figure class="acc-card-media">`. The `.feature` span/dark treatment and
  the old photo caption were removed for uniformity. Citation carries the approved
  framing verbatim: “Selected through a highly competitive process from thousands of
  applications across the 56 Commonwealth countries; presented at Asprey, London,
  and received at St James's Palace in October 2026.” (The old card did not contain
  the framing line; it lived in the proof band — it is now on the card as briefed.)
- **One Young World 2026** — from-behind handshake photo removed (img reference only;
  `assets/oyw-chanel.webp` stays in the repo). Citation trimmed to one line; the
  “sponsored by Chanel” clause was dropped with the photo to keep the one-line form.
- **Toronto Community Champion 2025** — conformed to the same structure (was already
  text-led); citation reworded to third person to match the card set.
- **Scarborough Walk of Fame 2024** — glitched recipient-card graphic removed:
  img reference deleted **and `assets/walk-of-fame-recipient-card.webp` deleted from
  the branch**. Typeset card instead.
- **CharityVillage 2021** — clashing rosette removed: img reference deleted **and
  `assets/charityvillage-badge.webp` deleted from the branch**. Typeset card instead.

## 5. A7 — Testimonials rebuild (lines 822–838)
Sources: `testimonial-mining-oct20.md` only — the two quotes already published, rebuilt
to the brief's exact texts and the name + role + org attribution norm. Order swapped
so the organizer quote leads.

- **RETIRED:** the published Laura Mercieca quote containing “keeping talking”
  (“They loved your visit and keeping talking about you.”) and the “Your discussion
  about this yesterday was perfect.” fragment. Per the mining file, “keeping talking”
  is a typo in Mercieca's original email, not a site transcription error, so it was
  not silently corrected — the quote is replaced.
- **RETIRED:** the Erica Procter quote as previously published (“The roundtables were
  the most highly rated part of the evening!” — a collective survey line about all
  roundtables, per the mining file).
- **NEW 1:** Erica Procter, Founder & Executive Director, FUEL (Fuel Change) — July 2023:
  “I wanted to send a huge thank you for coming to the FUEL event last week — and for
  hosting a roundtable. We have had great feedback about the event and I was so happy
  that you were a part of it.”
- **NEW 2:** Laura Mercieca, Teacher, Toronto District School Board — May 2022:
  “It was so great to see you yesterday, and thank you so much again for coming in to
  work with the class!”
- No other quotes added; no outreach; nothing invented.

## 6. A9 — Organizer bio block (Media section, lines 907–920; JS lines ~1149–1162)
Added a compact “For organizers” subsection directly after the Media downloads row:
copy-ready **Short bio — 50 words** (`#bio-short`) and **Long bio — 141 words**
(`#bio-long`), third person, facts only from the page (Leadership Advisor & Speaker;
Founder & Executive Director of The Good Guides; QECT 100 Young Leaders Awardee 2026;
Scarborough Walk of Fame Rising Star 2024; 10,000+ youth mentored since 2020;
5,000+ reached through talks; Toronto, Canada). Each bio has a small **Copy** button
(`.copy-bio-btn`, `data-copy-target` → the bio's id).

**JS added (for wave 2's awareness):** a ~13-line helper inside the main script —
click handler on `.copy-bio-btn` that copies the target element's text via
`navigator.clipboard.writeText`, then flips the button label to “Copied” for 1.6 s.
No other JS changed.

---

## 7. NEW CSS CLASSES INTRODUCED — for the wave-2 builder

No styles were written for any of these in wave 1 (per the wave split). Intended styling:

| Class | Element | Intended styling (wave 2) |
|---|---|---|
| `.acc-card-media` | `<figure>` — QECT card-top image (only instance) | First child of the card, full card width; **fixed aspect ratio** (suggested 4/3) with `overflow:hidden`; inner `img` fills it with `object-fit:cover`. Replaces the old `.acc-photo` treatment on this card. |
| `.acc-body` | `<p>` — awarding-body line on all 5 accolades cards | Distinct from the citation paragraph: suggested small, semibold, green or muted, tight margin under the `h3` (e.g. 13.5–14px, letter-spaced or uppercase at wave 2's discretion within the type system). |
| `.organizer-bios` | `<div>` — “For organizers” container in Media | A contained subsection block consistent with `.kit-band` (surface/border/radius family), spaced below the downloads row. |
| `.organizer-bio-note` | `<p>` — intro line under “For organizers” | Muted secondary text, ~15px. |
| `.organizer-bio` | `<div>` — wraps each label + bio text + copy button | Separated per bio (top border or spacing); bio text should read as copy-ready prose. |
| `.organizer-bio-label` | `<p>` — “Short bio — 50 words” / “Long bio — 141 words” | Small label treatment in the kicker family (uppercase/tracked or bold small text). |
| `.copy-bio-btn` | `<button type="button">` — Copy buttons | Small secondary button: outline/ghost weight, clearly subordinate to the gold CTAs; needs a `:focus-visible` state and a pressed/“Copied” state is handled by JS label swap only. |

New IDs (not classes): `#bio-short`, `#bio-long` — targets of the copy helper via
`data-copy-target`.

**Markup removed — CSS now orphaned, for wave 2 to prune or repurpose (not edited in wave 1):**
`.cta-band` / `.cta-in`, `.booking-band`, `.acc.feature` (+ its descendant rules),
`.acc-photo` / `.acc-photo.badge` / `.acc-photo figcaption` (no longer used by any card).

## 8. Validation performed
- Both JSON-LD blocks parse (`python json`); FAQPage mirrors the visible FAQ exactly (6/6, string-equal).
- HTML parser pass: no unclosed/stray tags.
- Every remaining `assets/` href/src resolves to an existing file (10 refs, 0 missing);
  all three PDF downloads resolve.
- `grep`: “public record” ×1 (footer); each signature talk title ×1; “keeping talking”,
  “never an assistant”, both deleted asset names and the OYW photo reference: 0.
- Main script passes `node --check`.
- Figures unchanged everywhere: 1 of 100 / 10,000+ / $1M+ / 5,000+. No résumé/CV
  added; no pricing added; pronunciation line untouched (hero only); positioning
  “Leadership Advisor & Speaker” untouched.

---

# List A — Wave 2: Design System (Oct 22, 2026)

Branch: `list-a-preview-oct22` · Files: `index.html` (systems/technical pass only — no copy
changed except the directed heading conversion), `assets/hero-headshot.webp` (re-export),
plus two new image variants. Builds on wave 1 (HEAD was `82ac9d4`).

## 1. A5 — Type system

**Font tokens** (the only literal stacks left in the stylesheet are the token definitions
themselves and the Google Fonts URL):

| Token | Value |
|---|---|
| `--font-display` | `"Playfair Display",Georgia,serif` |
| `--font-body` | `"Source Sans 3",system-ui,sans-serif` |

All 17 stack re-declarations replaced with the tokens.

**8-step scale** — every `font-size` declaration now resolves to exactly one of:
`12 / 14 / 16 / 17 (body) / 20 / 24 / clamp(32px,4.6vw,46px) h2 / clamp(46px,6vw,64px) h1`.
Roles: lede = 20; card body = 16; captions/meta = 14 or 12; kickers/labels = 12; prose = 17.
Mapping notes: all six half-pixel sizes (11.5/12.5/13.5/14.5/15.5/16.5/17.5) rounded to the
nearest step; the three off-scale clamps (roleline, startline, philosophy `.big`) and the
`1.08rem`/`.78em` one-offs mapped onto steps (roleline → 20, startline → 24, `.big` → the h2
clamp); the fixed 48px mobile h1 override deleted (the h1 clamp's 46px floor covers it).
Verified: distinct `font-size` values in the stylesheet = exactly the 8 steps.
Google Fonts: Playfair 500 (normal + italic) dropped from the css2 URL; kept weights are
600/700/800 + italic 600 (Playfair) and 400/600/700 (Source Sans 3) — what the CSS uses.

**Heading conversion** (the one directed copy touch): all 11 section `.kicker` elements
deleted (and the `.kicker` rule with them); every section H2 is now a plain serif label at
the h2 step — About · What I bring · Honours and recognition (trailing period dropped) ·
Advisory & speaking · Signature talks · Selected appearances · Testimonials · Media ·
Questions · Contact & enquiries. The Typical Engagement card's `<h3>` was promoted to
`<h2>A typical engagement</h2>` (styled at the 24 step via `.typical h2`). Philosophy gained
`<h2>The philosophy</h2>`; the big statement line stays a `<p>` (now at the h2 clamp).
Hero eyebrow/role lines untouched. *Noted consequence:* the FAQ answer "What does an
advisory engagement look like?" (and its JSON-LD mirror) still quotes the old heading text
"Advisory — a typical engagement" — left as-is because copy was out of wave-2 scope; flag
for a wave-3 copy decision.

## 2. A6 — Spacing system

| Token | Value | Use |
|---|---|---|
| `--space-1` … `--space-6` | 8 / 16 / 24 / 32 / 48 / 64px | general rhythm |
| `--gap-card` | 18px | all card-grid gaps (was 6 separate `gap:18px`) |
| `--card-pad` | 28px | one padding for acc/offer/talk/tquote/enquiry/typical/kit + organizer-bios |
| `--section-pad` | 88px (60px at ≤640) | `section{padding:var(--section-pad) 0}` for ALL sections |

All 9 inline styles removed (6× `padding-top:0`, `margin-top:22px` → `.two .after-pull`,
`margin-top:0` → `.talks{margin-top:0}`, footer brand span → `.foot-brand`); zero `style=`
attributes remain. Hero: `.hero-in` padding 72px top / 96px bottom desktop (40/56 mobile).
`.stages-grid` 820px cap removed — its inner wrapper is now a two-column grid at desktop
(appearances list | engagements), one column at ≤900. Card grids use `align-items:stretch`
(accolades, testimonials, watch; offers/talks stretch by grid default) — rows are level.

## 3. A3 — Colour restraint (dosage only; palette unchanged)

- `--surface2` (#EFE8D3) now survives in exactly one component: the Contact section
  (footer-adjacent). Accolades → cream page ground, Philosophy → white, kit-band → white.
  Green remains structure: nav, proof band, contact band context, footer.
- Hero H1 surname and the Philosophy emphasis set in ink (italic kept).
- `.btn-gold` renamed `.btn-primary` everywhere (CSS + 4 HTML uses) and redefined as the
  one gold family: gold fill + ink text, hover #FFD34D — the old nav-only override is gone
  because the definition is now uniform. `.btn-dark` / `.btn-outline` remain secondaries.
- Gold decoration deleted: list bullets are now 6px green squares (offer + engagements);
  the five 2px gold top-rules (`.pull`/`.bring`/`.faq`/`.step`/`.engagements`) are 1px
  `var(--line)` hairlines; testimonial quote glyph → 24px green-dark; play buttons →
  green-dark disc with cream triangle (hover green); card hovers → `border-color:var(--green)`
  with the translate lift removed (also `.bring`/`.direct`/`.watch-card`). Nav chrome gold
  rgba borders → cream rgba; the hero's gold radial glow removed; mobile-menu CTA now uses
  `--gold-on-green` (4.55:1 on green, AA) instead of raw gold. Gold-on-green text remains
  only inside green bands (proof label, footer links, menu CTA).

## 4. A4 — Stillness

- Count-up removed entirely: JS block deleted, all 8 `data-countup/-prefix/-suffix/-format`
  attributes removed. The four proof figures are static text, verified byte-exact in the
  render: `1 of 100` · `10,000+` · `$1M+` · `5,000+`.
- Reveal system removed entirely: `@keyframes rise-in(-sm)`, all `html.js .reveal/.rv` rules,
  the hero entrance cascade, the IntersectionObserver + sweep/`setInterval` machinery
  (~4.3 KB of JS), the head `classList.add('js')` gate script, and every `rv`/`reveal` class
  token stripped from markup (verified: zero tokens remain; spot-checked proof label, press
  strip, cards, bios, contact). Kept: mobile-menu toggle, video facades, copy-bio helper,
  print stylesheet, the global `prefers-reduced-motion` rule.

## 5. A9 — Technical

- **Focus:** gold outline replaced with a two-tone ring — `box-shadow:0 0 0 2px #fff,
  0 0 0 5px var(--green-dark)` on light grounds; on green grounds (nav, mobile menu, footer,
  proof) the ring inverts to green-dark inner + white outer, so the indicator is ≥3:1
  against every ground it can sit on.
- **Breakpoints 9 → 4:** width queries now use only `900 / 640 / 480` max-width and
  `901` min-width (1100 is in the allowed scale, unused). Remaps: nav 920→900 (+921→901),
  prose two-col 820→900, contact 860→900, hero/proof/bring/faq 820→900, media rows 700→640,
  steps 560→640, press + hero-eyebrow + accolade single-col 600→640.
- **Dead CSS deleted (35 line-rules + 2 segments):** the orphaned form system
  (`form`, `form label`, `form input/select/textarea`, `form textarea`, `.frow` + its media
  query, `.sent`), `.factlist` (4), `.gtk` (2), `.btn-ghost` (2), `.hero-note` (2 + its
  animation references), `.serif`, `.media-item` (2), `.media-video`, `.stages-video
  figcaption .cue`, `.talk .tspec`, the duplicate `.talk-aud`, `.kicker`, and wave-1's
  orphans (`.cta-band`/`.cta-in` 4 rules, `.booking-band` 3, `.acc.feature` + `.acc-photo`/
  `.badge` segment of 13 rules). Print stylesheet selector list pruned to match. Post-pass
  grep: every remaining CSS class selector matches the HTML — the sole exception by design
  is `.open`, the mobile menu's JS-toggled state class (present via `classList.toggle/remove`
  in the kept script).
- **Head:** `<meta name="theme-color" content="#2D6B38">` and `og:image:alt` added.
- **Hero image ratio:** `.portrait-frame img` aspect-ratio aligned to `764/955` (was 764/968).
- **Validity:** the four media rows' `<span><h3>…` wrappers are now `<div>`; desktop nav
  landmark is `aria-label="Primary"` (mobile menu keeps "Sections").
- **Wave-1 classes styled** inside the token system: `.acc-card-media` (full-bleed card-top,
  fixed 4/3, `object-fit:cover`), `.acc-body` (14px semibold green-dark), `.organizer-bios`
  (white panel, `--card-pad`), `.organizer-bio` (hairline-separated), `.organizer-bio-label`
  (12px tracked uppercase green), `.organizer-bio-note` (16px ink2), `.copy-bio-btn` (small
  outline secondary, 14px).

## 6. Images

- `assets/spotlight-candid-726.webp` generated (726×908, WebP q82); hero img now carries
  `srcset="…726w, …1290w"` with `sizes="(max-width: 900px) 240px, 363px"` — the browser
  picked the 726w variant at desktop in the smoke render.
- `assets/qect-award-660.webp` generated (660×660, WebP q82); accolade img carries
  `srcset="…660w, …1080w"` with card-matching `sizes` — the 660w variant was picked.
- `assets/hero-headshot.webp` re-exported from the same photograph at
  `…/linkedin-refresh-oct19/profile-option-1-headshot.jpg` (800×800): centre-cropped to the
  current 435:463 framing at full height → **751×800**, WebP q82 (8.5 KB → 20 KB, now 2.5×
  the 300px display width). `width`/`height` attributes and the `.contact-photo` CSS ratio
  updated to 751/800. Same photo, same crop intent — resolution only.
- `making-a-difference-thumb.webp` **not touched** (per brief — broadcast-source re-export
  blocked; no upscale, no substitute).

## 7. Validation

- `html.parser` pass: no errors, no unclosed tags. Extracted script passes `node --check`.
  CSS braces balanced (306/306).
- Greps: zero half-pixel font sizes; distinct font sizes = the 8 steps exactly; zero
  `data-countup`; zero inline `style=` attributes; width breakpoints ⊆ {901, 900, 640, 480};
  zero dead class selectors (`.open` state class excepted, see §5); zero `btn-gold`/`kicker`/
  `cta-band`/`booking-band`/`acc-photo` strings.
- Smoke render (local `http.server` + Playwright, full-page 1280/768/375, screenshots in
  `/tmp/wave2-shots/`): **no horizontal overflow at any width**
  (`scrollWidth == innerWidth` at 1280, 768 and 375); computed section pad 88px desktop /
  60px at 375; hero padding 72/96; card pad 28px; primary button renders gold #F5B921 with
  ink text; stages grid renders 514px + 514px columns at desktop, single column ≤900; all 12
  section H2s read as the new plain labels; all six images load (lazy ones on scroll) and
  both srcset variants are selected by the browser. No page JS errors (the only failed
  requests were external — Google Fonts CSS and GoatCounter through this VM's proxy —
  the page renders on its tokenized Georgia/system-ui fallbacks when they fail).

---

# Fix Round — Visitor-Eye Gate Failures (Oct 22, 2026)

Branch: `list-a-preview-oct22` · File edited: `index.html` only. CSS/layout only — no copy
changed except the F5 overlay de-duplication directed by the gate spec (the duplicated
meta line removed from the two Media watch overlays; it remains once, in each card body).
All wave-2 system rules kept: type scale, tokens, breakpoints 900/640/480, one card padding.
Spec: `gate-visitor-eye.md` (Gate 2 of 4, FAIL on F1–F5 + LOWs). Screenshots of the fixed
regions: `/tmp/fix-shots/` (1280/768/375 × accolades, press, watch, contact, kit, hero,
testimonials, speak-band).

## F1 — Contact enquiry panel sized to content (was 56% empty at 1280)
`.contact-grid` gains `align-items:start`; the "Send an enquiry" panel no longer stretches
to the left column's height. Verified nothing else in the grid depended on the stretch (the
left `.direct` column is self-sizing; at ≤900 the grid is single-column and the rule is inert).
**Measured:** panel 870px tall / 56% void → **408px / 7% void** at 1280 (the residual 29px is
the card's own bottom padding + border). At 375 the stacked panel is 602px / 5% void.

## F2 + F4 — Accolades: QECT feature card + uniform 4-card grid
- The QECT card leaves the uniform grid and becomes a full-width **feature card**
  (`.acc-feature` / `.acc-feat`): photo left, full-bleed on three sides with the existing
  square source filling a 422×422 crop at 1280 (`.acc-feat-media`, `object-fit:cover`),
  text right in a vertically centred column (`.acc-feat-body`). At ≤900 it stacks: photo
  becomes a 16/9 banner on top, text below. All QECT copy verbatim, including the approved
  framing line; the `img` `sizes` updated to the new geometry (430px desktop / full card
  width ≤900). The now-unused `.acc-card-media` rules were removed.
- The remaining four honours sit in their own `.acc-grid`: **4-across at desktop →
  2+2 at ≤900 → stacked at ≤640** (base changed from `repeat(3,1fr)` to `repeat(4,1fr)`;
  grid top margin is now `--gap-card`, the feature block carries the section's 36px).
- Every accolade card is now `display:flex;flex-direction:column`; the source link is
  pinned to the card bottom with `margin-top:auto` above a 1px `var(--line)` hairline
  (`padding-top:12px`), so residual space reads as structure.
**Measured (text-void = gap between last text line and the pinned link / card foot):**
at 1280, one row of four, all cards 461px — One Young World 19%, Toronto Community
Champion 21% strict (85px true blank ≈ 18% net of the citation's own 12px bottom margin;
it is the one card with no source link to pin), Walk of Fame 19%, CharityVillage 3%.
At 768 the grid is exactly **2+2, nothing stranded** — voids 4% / 16% / 11% / 3%.
At 375 all four stack, voids ≤4%. Feature card at 1280: 424px tall, photo fills its full
height; at 768/375 the banner crop is a clean 16/9.

## F3 — Press strip: gutter restored, fifth item no longer stranded
Root cause: `.press-in{padding:22px 0}` sat later in the cascade than `.wrap{padding:0 22px}`
at equal specificity, zeroing the horizontal gutter — the strip ran edge-to-edge (left = 0px)
at 375/768. `.press-in` (and its ≤640 variant) now sets only `padding-top/bottom`, so the
standard `.wrap` 22px gutter applies at every width. The ≤640 2-column grid's special case
(`grid-column:1/-1;justify-self:center` on the last item) is removed: the fifth item now sits
**left-aligned in column 1 of the grid rhythm**.
**Measured:** padding-left computes to 22px at all widths. 375: items at x=22 in a 2+2+1
grid, fifth item left-aligned. 768: items inset (x=22), natural flex wrap, fifth item
left-aligned on row 2. 1280: unchanged — label + all five items on one row, as the gate
called perfect.

## F5 — Media watch overlays de-duplicated
Both `.watch-grid` facades now carry only the play disc + the short label ("Watch the
segment" / "Watch the panel") over the existing bottom scrim. The `<small>` meta line
(outlet · date · duration) is removed from both overlays — it stays once, in each card's
`figcaption`. The Global News label no longer collides with the thumbnail's baked-in
broadcast banner (verified in the 1280 screenshot). Card body copy untouched.
Note: the Selected Appearances speak-band facade is a different card, not flagged by the
gate, and is untouched — its `.vid-label small` rule is retained for it.

## LOWs
- **Testimonials (F6):** `.tquote` is now flex-column with the attribution pinned to the
  bottom (`figcaption{margin-top:auto}`; the blockquote carries the 18px minimum gap).
  At 1280 both cards are 290px with the caption 29px from the card foot (= padding +
  border) — the second card's blank lower third is gone.
- **Tablet hero portrait (F7):** at ≤900 `.portrait-col` is centred in its column
  (`width:100%;align-self:center;margin:24px auto 0`). Measured centre offset at 768:
  **0px** (was floated left with an empty right half).
- **Media downloads pills (F8):** the three pills live in `.kit-band` (the page's `.dl-row`
  instances each hold a single link). `.kit-band .sp` now takes a full row and the three
  `.btn` pills share one even row beneath it (`flex:1 1 0`, equal widths/heights, band is
  `align-items:stretch`); at ≤640 each pill takes a full row. **Measured:** 1280 — 3 across
  × 323px; 768 — 3 across × 206px; 375 — stacked 1-per-row × 273px. Never 2+1.

## Validation (gate method mirrored)
Served the worktree (`python3 -m http.server 8903`), rendered with Playwright at
1280/768/375 with a slow end-to-end scroll before measuring:
- `scrollWidth == innerWidth` at all three widths (1280/1280, 768/768, 375/375).
- All 6 `<img>` elements `complete=true`, `naturalWidth>0` at all widths.
- HTML parser pass clean; CSS braces balanced (315/315 after the restored `.vid-label
  small` rule); no orphaned selectors introduced (`.acc-card-media` removed with its
  markup; `.acc-feature/.acc-feat/.acc-feat-media/.acc-feat-body` added with theirs).
- Region screenshots in `/tmp/fix-shots/` eyeballed: feature card, 4-across and 2+2
  accolade grids, press strip at 375/768/1280, both watch cards, contact panel,
  testimonials, kit band, 768 hero — all as measured above.

## Gate fix round (post-writing-gate, coordinator-applied)
Writing gate (a6eba2b) returned FAIL on three items; fixed in the fix-round commit:
- F1 Contact lede: dropped the trailing "— and I'll reply myself" so the answered-personally promise is stated exactly once.
- F2 About after-pull: "carried me to London as one of the QECT 100 Young Leaders" → "carried me to London" (honour keeps its proof-band + accolades homes; resolves the wave-1 flagged retention).
- F3 Walk of Fame media-row blurb: first-person claim + 10,000+ re-assertion → third-person record descriptor ("founder of The Good Guides, the youth-led mentoring organization he built in Scarborough from 2020.").
- Warning fixes: Toronto Community Champion citation re-moored ("…, recognizing the mentors and young people doing the work."); long-bio spelling normalized to the page's z-forms (organization / Organizers) — word count unchanged (141).
