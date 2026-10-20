---
name: V Drywall
description: Drywall and painting in Northern Michigan, in Ellie's calm band style with flag navy and flag red from the shop sign.
colors:
  flag-red: "#b31942"
  flag-red-bright: "#c8234f"
  red-ink: "#b31942"
  flag-navy: "#0a3161"
  deep-navy: "#071d3a"
  paper: "#f4f6fb"
  card-white: "#ffffff"
  field-tint: "#e6ecf5"
  ink: "#0a1f3f"
  body-slate: "#2a3a4c"
  soft-slate: "#4a5868"
  on-dark: "#f4f7fb"
  on-dark-soft: "#c9d7ea"
  focus-navy: "#0a3161"
  error-red: "#a3141f"
typography:
  display:
    fontFamily: "Cal Sans, Avenir Next, Segoe UI, system-ui, sans-serif"
    fontSize: "clamp(42px, 12vw, 80px)"
    fontWeight: 400
    lineHeight: 1.02
    letterSpacing: "-0.005em"
  headline:
    fontFamily: "Cal Sans, Avenir Next, Segoe UI, system-ui, sans-serif"
    fontSize: "clamp(30px, 7.6vw, 48px)"
    fontWeight: 400
    lineHeight: 1.08
    letterSpacing: "-0.005em"
  title:
    fontFamily: "Cal Sans, Avenir Next, Segoe UI, system-ui, sans-serif"
    fontSize: "clamp(21px, 5.8vw, 26px)"
    fontWeight: 400
    lineHeight: 1.15
  lede:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(17px, 4.6vw, 19px)"
    fontWeight: 400
    lineHeight: 1.7
  body:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Helvetica Neue, Arial, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.7
  label:
    fontFamily: "Cal Sans, Avenir Next, Segoe UI, system-ui, sans-serif"
    fontSize: "18px"
    fontWeight: 400
    lineHeight: 1.2
rounded:
  field: "10px"
  card: "24px"
  pill: "999px"
spacing:
  gutter: "20px"
  gutter-desktop: "40px"
  section: "64px"
  section-desktop: "96px"
  stack: "16px"
  field-gap: "20px"
  column-gap: "64px"
components:
  button-primary:
    backgroundColor: "{colors.flag-red}"
    textColor: "{colors.card-white}"
    typography: "{typography.label}"
    rounded: "{rounded.pill}"
    padding: "0 26px"
    height: "56px"
  button-primary-hover:
    backgroundColor: "{colors.flag-red-bright}"
    textColor: "{colors.card-white}"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.on-dark}"
    typography: "{typography.label}"
    rounded: "{rounded.pill}"
    padding: "0 26px"
    height: "56px"
  input-field:
    backgroundColor: "{colors.field-tint}"
    textColor: "{colors.ink}"
    typography: "{typography.body}"
    rounded: "{rounded.field}"
    padding: "13px 14px"
    height: "52px"
  chip:
    backgroundColor: "{colors.field-tint}"
    textColor: "{colors.ink}"
    typography: "{typography.body}"
    rounded: "{rounded.pill}"
    padding: "0 18px"
    height: "48px"
  chip-selected:
    backgroundColor: "{colors.flag-navy}"
    textColor: "{colors.card-white}"
  form-card:
    backgroundColor: "{colors.card-white}"
    rounded: "{rounded.card}"
    padding: "clamp(20px, 5vw, 32px)"
  service-row:
    backgroundColor: "transparent"
    textColor: "{colors.on-dark}"
    typography: "{typography.title}"
    height: "76px"
  float-text:
    backgroundColor: "{colors.flag-red}"
    textColor: "{colors.card-white}"
    rounded: "{rounded.pill}"
    size: "60px"
---

# Design System: V Drywall

## Overview

**Creative North Star: "The Shop Sign, Calmly"**

This is Ellie's house **calm band style** (`~/.claude/skills/pitch-site/references/calm-photo-style.md`), recoloured from the crew's own shop sign: flag navy and flag red on white. Full-bleed bands alternate paper and navy so every new section is obvious at a glance on a phone; the order shipped is navy photo hero, paper, navy, paper, deep textured navy, paper, deep textured footer. Shapes are soft and borderless, type is one display webfont over a system body, and motion is limited to one letter bounce on the hero H1 and one quiet fade-up below the fold.

The page is low-density and phone-first: one idea per band, a headline, at most a lede, and one control group. The crew's real primed-garage photo carries the hero under a navy overlay, and the same photo language (navy bottom gradient, white title) returns in the work band. Nothing is decorative that isn't from the business itself: the colours are the sign, the photo is their job.

The build departs from the house style in three deliberate, contrast-driven ways, all recorded as rules below: the warm accent is a red rather than a gold, so text on the accent fill is **white**, not navy (navy on this red fails contrast); there is **no accent-coloured phrase on dark bands** (red on navy fails); and the accent phrase instead appears on **paper** headings, set in red ink.

**Key Characteristics:**
- Calm band style: paper / flag navy / deep navy with faint 135deg line texture, full bleed, alternating.
- One accent, flag red, used as a fill with white text, and as red-ink text on paper only.
- Cal Sans display at weight 400 for headings, buttons, labels and phone numbers; system stack body at 16/1.7.
- Soft, borderless forms: 24px cards, full pills, 10px tinted fields.
- Motion: hero H1 letter bounce-in, a 12px fade-up for content below the first screen, a sliding text circle. All off under reduced motion.

## Colors

Flag navy and flag red on cool off-white paper, taken from the crew's shop sign; two navies carry the dark bands and one red carries every action.

### Primary
- **Flag Red** (`flag-red`): the one accent, always a fill. Primary pill buttons ("Get a quote", "Text this to us"), the floating text circle, and the service-row arrow circle on hover or focus. Text and icons on it are white (6.4:1).
- **Bright Flag Red** (`flag-red-bright`): hover state of the primary button only, on pointer devices.
- **Red Ink** (`red-ink`): red as text or icon on light grounds, at 5.9:1 on paper. Phone icons, the accent phrase in paper-band headings, hover colour of phone links. Same hue as the fill today; kept as its own token so the text role can darken without moving the fill.

### Secondary
- **Flag Navy** (`flag-navy`): the brand blue. Hero ground under the photo overlay, the services band, the work photo frame, the Facebook row, the selected chip, the V mark tile, text selection.
- **Deep Navy** (`deep-navy`): the darkest band, always paired with the line texture. Quote band and footer, and the dark end of every photo gradient.

### Neutral
- **Paper** (`paper`): the page ground and the header. Never black, never pure white.
- **Card White** (`card-white`): the quote form card on deep navy, and text on red and navy fills.
- **Field Tint** (`field-tint`): inputs, chips and the secondary "Copy message" button on the white card. Its own token because paper on white is about 1.08:1.
- **Ink** (`ink`): headings, labels and input text on light grounds.
- **Body Slate** (`body-slate`): running text on light.
- **Soft Slate** (`soft-slate`): ledes, hints, the secondary phone number, the "opens your messages" note.
- **On Dark** (`on-dark`) and **On Dark Soft** (`on-dark-soft`): headings and running text on navy and deep navy.
- **Focus Navy** (`focus-navy`): the 3px outline for hover and focus on form controls and paper-band links; switches to white on navy, deep, hero and footer.
- **Error Red** (`error-red`): field border and plain-sentence error text in the form.

### Named Rules
**The White-On-Red Rule.** Anything set on a flag-red fill is white. Navy on this red fails contrast. This is the deliberate deviation from the house style's navy-on-accent rule, which assumes a gold.

**The Paper-Only Accent Phrase Rule.** A heading's closing phrase may be set in red ink ("Hung, finished *and primed.*", "Any questions? *Give us a call.*") only on paper bands. Dark-band headings stay entirely on-dark: red text on navy fails contrast. This reverses the house style, which puts the accent phrase on dark bands only.

**The Red Is Action Rule.** Red fills mark something you can press: a primary button, the text circle, an arrow that has become active. Red on navy is fine as a fill under white; it is never text.

**The Textured Deep Rule.** Deep navy always carries the 135deg line texture (`rgba(255,255,255,.035)` 1px lines every 23px), kept at about 4% white so it never reads as lines through text. Flag navy is always flat.

## Typography

**Display Font:** Cal Sans (with Avenir Next, Segoe UI, system-ui)
**Body Font:** system stack (-apple-system, BlinkMacSystemFont, Segoe UI, Helvetica Neue, Arial)

**Character:** A friendly, round geometric display at a single regular weight over the phone's own reading face. Cal Sans does all the talking that isn't a sentence: headings, buttons, labels, the wordmark, phone numbers.

### Hierarchy
- **Display** (400, clamp 42-80px, 1.02): the hero H1 only, max 12ch, white on the photo. Drops to clamp(36px, 9vh, 52px) on landscape phones so the button stays on screen.
- **Headline** (400, clamp 30-48px, 1.08, -0.005em, balanced): every band's H2.
- **Title** (400, clamp 21-26px, 1.15): service rows and the photo card title; the Facebook row sits just below at clamp 19-22px.
- **Lede** (system, clamp 17-19px, 1.7): one-line or short paragraph under a headline, max 40ch, soft slate on paper, on-dark-soft on navy. The hero promise is the same role at clamp 17-20px / 1.5, max 30ch.
- **Body** (system, 16px, 1.7): running text and inputs. Inputs never go below 16px.
- **Label** (Cal Sans 400, 18px): form labels and legends, and button text at 18px / 1. Phone numbers use the display face too: 17-20px in the header, clamp 30-52px for the closing number.

### Named Rules
**The One Weight Rule.** Cal Sans is used at 400 only; hierarchy comes from size, not weight. Bold appears only inside body copy (the hero promise's quoted line, at 600).

**The Display-For-Doing Rule.** Every control label (buttons, form labels, service rows, phone links) is set in Cal Sans so actions read as part of the voice, not as UI chrome.

## Layout

Single column on phones inside a 1160px max container with a 20px gutter (40px from 760px). Bands pad 64px top and bottom, 96px from 760px; heading and lede stack at 16px inside a 640px max head block. From 1024px, bands that hold a head and a body split into two columns with a 64px gap (head 1fr against body 1.2fr to 1.5fr); the quote band's head goes sticky at 40px; the work photo spans both rows on the right. The hero copy pads 64/72px on phones and 112/128px on desktop, and its buttons go from full-width stacked to a side-by-side row with 220px minimum width.

Breakpoints are 760px (desktop rhythm), 1024px (two-column bands), and a landscape-phone query at max-height 500px. Hover styles live only inside `(hover: hover)` so taps never leave them stuck. Every tap target is 44px or taller.

## Elevation & Depth

Flat. Depth comes from band colour and the photo overlays, not shadows. The only shadow in the system is the floating text circle, which lifts above all content because it is the one element that moves over it.

### Shadow Vocabulary
- **Float lift** (`box-shadow: 0 10px 28px rgba(8,24,46,.3)`): the floating text circle only.

### Named Rules
**The Band-Not-Shadow Rule.** Separate things by changing band or by a 1px 14% white rule between service rows; never by a card shadow.

**The Navy Veil Rule.** A real photo always sits under a navy gradient: top-to-bottom deep/navy/deep (0.8 / 0.72 / 0.88) on phones, left-to-right 0.88 fading to 0.42 on desktop so the job shows on the right while the copy side stays dark. Photo cards use a bottom 45% gradient to deep navy at 0.78 under a white title.

## Shapes

Soft and borderless. Large containers round at 24px (the form card, the work photo), the Facebook row at 20px, fields at 10px, and everything pressable that isn't a field is a full pill or a circle (buttons, chips, arrow circles, the text circle). Borders appear only as state: a 2px transparent border on fields, chips and buttons turns focus navy on hover or focus, or error red when invalid; the ghost button's 2px border is its whole shape. The V mark is a 10px-rounded navy tile with a 5px red base stripe, the sign's flag in miniature.

## Components

### Buttons
Round, confident, Cal Sans.
- **Shape:** full pill (999px), 56px tall, 26px side padding, 20px icon with 10px gap.
- **Primary:** flag red fill, white Cal Sans 18px. Full width inside the form.
- **Hover / Focus:** hover brightens to bright flag red (pointer only); inside the form, hover and focus also draw the 3px focus-navy outline at 3px offset. Press scales to 0.98.
- **Ghost:** transparent with a 2px 75% on-dark border and on-dark text, used on the hero only; hover firms the border to white over a 10% white wash.
- **Secondary (field):** the "Copy message" button is a pill on field tint with ink text, 48px.

### Chips
- **Style:** field-tint pills, 48px tall, 18px padding, ink system text 16px; the checkbox is visually hidden and the label is the chip.
- **State:** checked fills flag navy with white text; hover draws a focus-navy border; keyboard focus draws an offset outline (a border would vanish on the navy fill). Tapping a service row pre-checks its chip.

### Cards / Containers
- **Corner Style:** 24px.
- **Background:** white form card on deep navy; navy-framed photo card at 4:3 on paper.
- **Shadow Strategy:** none (see Elevation).
- **Border:** none.
- **Internal Padding:** clamp(20px, 5vw, 32px) with 20px between fields.

### Inputs / Fields
- **Style:** field-tint fill, 2px transparent border, 10px radius, 52px tall (textarea 110px, vertical resize), 16px system text in ink, navy caret, placeholder #5a6878.
- **Focus:** border turns focus navy; hover does the same on pointer devices.
- **Error:** border turns error red and stays red through focus; a plain-sentence error line in error red appears below.

### Navigation
- **Header:** paper strip, 64px (76px desktop), V mark tile plus Cal Sans wordmark on the left, tap-to-call number with a red-ink phone icon on the right; the number turns red ink on hover. No menu.
- **Footer:** deep textured navy, one line of name and area, links in on-dark that underline at a 6px offset on hover. Bottom padding clears the floating circle and the safe area.

### Service Rows (signature)
The services band is a list of full-width links on flag navy, one per job, Cal Sans title size, 76px tall, separated by 1px 14% white rules. Each ends in a 44px arrow circle at 10% white; on hover or focus only the arrow changes, filling flag red with a white arrow (focus adds a white outline). The row itself never highlights. The Facebook row in the work band is the same pattern as a 20px-rounded navy slab.

### Floating Text Circle (signature)
A 60px flag-red circle, bottom right inside the safe area, opening a pre-written `sms:`. It slides up 120px into place over 0.35s `cubic-bezier(.2,.8,.2,1)` once the hero has scrolled away, and slides out while the quote form is on screen; when hidden it leaves the tab order and the accessibility tree. One circle, never a bottom bar.

### Not canonized
The build carries small eyebrow pills (red-dot labels above the hero H1 and three paper/deep headings) because the house style asks for them. They are a known anti-pattern conflict noted in the house style itself, so they are not a component of this system and new surfaces should not inherit them from this file.

### Motion
- **Hero H1 bounce-in:** letters slide in from 50px right, fading from 0, over 1s `cubic-bezier(.34,1.56,.64,1)`, 20ms apart, split in JS inside nowrap word wrappers; it waits up to 700ms for Cal Sans, then restores the plain heading on the last `animationend`. Hero H1 only.
- **Fade-up:** `.rise` content that starts below the first screen moves 12px up and fades in over 0.4s ease-out on entry. Everything is visible at rest, without JS, and under reduced motion.
- **State transitions:** 0.15s for field and chip borders, 0.2s for button and arrow colours.

## Do's and Don'ts

### Do:
- **Do** put white text and icons on every flag-red fill (6.4:1).
- **Do** use red ink for the accent phrase in paper-band headings only, and keep dark-band headings fully on-dark.
- **Do** alternate full-bleed paper and navy bands, and give deep navy the 135deg line texture at about 4% white.
- **Do** set headings, buttons, labels and phone numbers in Cal Sans 400; keep body and inputs on the system stack at 16px or larger.
- **Do** give fields and chips the field tint on white cards, never paper.
- **Do** put real job photos under the navy veil and check white text at 4.5:1 or better over them.
- **Do** keep hover styles inside `(hover: hover)` and every tap target at 44px or more.
- **Do** switch focus outlines to white on navy, deep, hero and footer.

### Don't:
- **Don't** set navy text on the red fill, or red text on navy or deep navy; both fail contrast.
- **Don't** use a gold or second warm accent; the sign's red is the only accent.
- **Don't** add card shadows; the floating text circle is the only lifted element.
- **Don't** letter-animate any heading but the hero H1, or leave content hidden at opacity 0 at rest.
- **Don't** highlight a whole service row on hover; only its arrow fills.
- **Don't** add a second body font or a bold Cal Sans.
- **Don't** replace the floating circle with a bottom bar.
