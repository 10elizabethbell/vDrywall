# V Drywall — handoff at ~60%

**Live:** https://10elizabethbell.github.io/vDrywall/ · **Repo:** https://github.com/10elizabethbell/vDrywall · **Built:** 2026-10-20 from Muse brief 2026-10-20 (Essex County Contractor Referrals post) · **Call Sheet:** added as `vDrywall` with the live link (Muse hadn't added it yet)

## What's built
- One page, phone first, in the calm band style: navy photo hero / paper "Every job" / navy services / paper work / deep textured quote form / paper close / deep footer.
- Palette from their shop sign (the Facebook profile photo): flag navy `#0a3161`, deep `#071d3a`, paper `#f4f6fb`, flag red `#b31942` as the one accent.
- Hero: their own job photo (the primed Bellaire garage) under a navy overlay. On desktop the overlay lightens on the right so the wall and window show. White text tested at 6:1 or better by pixel sampling (phone 6.1, desktop 7.8).
- H1 "Drywall done right in Northern Michigan" bounces in letter by letter. It waits up to 700ms for Cal Sans so the font doesn't swap mid-bounce. The fade-up runs on everything below the first screen. Under reduced motion and with no JS, everything shows at once (tested).
- Contact: (231) 676-9270 is in the header's top-right corner (tap to call), and both numbers are in the close. Service rows pre-pick the job in the quote form. The form writes a text to (231) 676-9270, with a "call us" line and a "Copy message" fallback. The floating text circle shows after the hero and hides at the form (tested).
- Facebook link under the work photo ("See more of our work on Facebook") and in the footer.
- Favicon, home-screen icon and the 1200x630 og.png all use the site's own "V" lettering on navy with a red stripe. There's no usable logo.

## Assumptions I made
- **Location: I put "Northern Michigan" in the H1 and close, against the brief's caution.** Muse flagged a mismatch: the post was in an Essex County NJ group, but the job was in Bellaire, MI. I found three more pieces of the business's own evidence:
  - The Facebook page lists "Ocqueoc".
  - Their profile photo is a shop sign with both phone numbers and "…74 US Hwy 23 North Millersburg, MI".
  - Both area codes (231, 989) are northern Michigan.
  - The NJ group looks like the odd one out. To revert, edit the H1, the close, the footer and the meta tags.
- **Name:** the site says "V Drywall", the Facebook page name. The sign reads "…VAN'S DRYWALL CONSTRUCTION", and its first letter is cut off (Evan's? Ivan's?). One email on the sign looks like "…vannolle…@icloud.com". **Confirm the real name with the owner before handing over.**
- **"We" voice** from the caption ("Our guys hung and finished the garage and we went in and primed it").
- **Promise** "We give 100% and do great work" comes from their Facebook bio: "Give 100% and do great work."
- **Texts go to (231) 676-9270**, the first number in the caption and on the sign. Nobody has confirmed it takes texts; the caption says "give us a call". The form's fallback shows the number to call.
- **White text on the red accent:** the calm style says navy text on accent fills, but navy on this red is about 2:1. On dark bands the accent phrase stays white, because red on navy also fails.

## Placeholders and gaps
- **Only one work photo** (2048x1536, from the group post). I blurred the licence plate on a truck outside. The trailer shows a partial brand ("TR…"); it's fine.
- **No email.** The sign shows two, but both are cut off. The footer has none until the owner gives one.
- No hours, prices, reviews, years in business, licence or insurance. The page says nothing about any of these.
- No before/after pairs.

## Questions for the owner
1. What's the business name exactly, the full name on the sign?
2. Which number should the website text and call? Does it take texts?
3. Which towns do you cover? (Bellaire, Millersburg, Ocqueoc, Rogers City…?)
4. An email for the footer?
5. More job photos, especially before/afters (bare studs, then primed walls)?
6. Are you licensed or insured, and how long have you been doing this? Only if you want those on the page.

## Ideas not built (yours to pick)
- **Signature motion (runner-up worlds):**
  1. A trowel swipe that skims mud across the hero, smoothing a rough seam as you drag. Best fit.
  2. A paint roller that rolls primer over grey board.
  3. Tape lines that draw along seams.
  4. A flag-stripe wave from the sign.
- **Before/after slider** once paired photos exist.
- A service-area line of towns once confirmed. Kept as plain text, never pills.
- **Impeccable findings kept by Ellie's choice:**
  - eyebrow pills (4: hero, Every job, Our work, Free to ask)
  - the H1 bounce-in
  - Cal Sans
  - the band texture (I added a detector ignore for the stripes in `.impeccable/config.json`)
  - the floating text circle (while you scroll services on a phone, it can sit over a row's arrow)
- **Left standing:**
  - The detector's "flat type hierarchy" warning on the small UI sizes (14/16/18/20). The display sizes carry the hierarchy.
  - "and primed." in red-ink on paper. It's 5.9:1, so it passes.

## Not verified
- Real-device tap and the SMS handoff on iOS and Android, including inside Facebook's in-app browser. The `sms:` body was tested by decoding only.
- Whether the clipboard copy works in Facebook's in-app browser. The number is always shown as well.
- WebKit was checked through Playwright, not on a real iPhone.
