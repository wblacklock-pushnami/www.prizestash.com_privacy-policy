# Creative Brief — Privacy Policy

**Source URL (recreate to the letter, then clean it up):** [https://www.prizestash.com/privacy-policy](https://www.prizestash.com/privacy-policy)
**Notes from tracker:** Legal Page
**Folder:** `pages/www.prizestash.com_privacy-policy/`
**Output file:** `index.html` (sibling of this brief)

---

## 1. Purpose

Long-form legal disclosure of data collection, use, sharing, and rights.

This page is a **like-for-like recreation** of `https://www.prizestash.com/privacy-policy` — every clause, field, headline, and link from the live page must appear in the rebuild. Pull the exact body copy and structure from the live page, then re-skin it using the design system below. Do not paraphrase legal text; copy it verbatim.

## 2. Content sections (in order)

1. Hero header — title 'Privacy Policy', updated date in small meta
2. Sticky in-page TOC
3. 1 — Information we collect
4. 2 — How we use information
5. 3 — Sharing & disclosure
6. 4 — Cookies & tracking
7. 5 — Third-party services
8. 6 — Your rights (link to CCPA page)
9. 7 — Data retention & security
10. 8 — Children's privacy
11. 9 — International transfers
12. 10 — Changes to this policy
13. 11 — Contact

> **Sourcing note:** open `https://www.prizestash.com/privacy-policy` and copy the actual text into the matching section above. If a section on the live page is missing here, add it; if a section here doesn't exist on the live page, drop it. Goal is exact content parity, cleaner presentation.

## 3. Layout

720px column, sticky TOC on desktop (left rail), inline on mobile. Highlight callouts for user rights and data-sharing in tinted card (`--purple-tint`).

## 4. Calls to action

Secondary buttons in 'Your rights' section linking to CCPA Right-to-Access and Right-to-Delete pages.


## Shared Design System (apply to every page)

### Color tokens
```css
:root {
  --push-purple: #5C3DE4;   /* primary CTA, links, accents */
  --dark-purple: #312679;   /* hover, emphasis */
  --clear:       #F1F1F1;   /* page background */
  --ink:         #1E1E1F;   /* primary text — never pure black */
  --ink-2:       #4a4a4d;   /* secondary text */
  --line:        #d2d6e0;   /* hairline borders */
  --surface:     #FFFFFF;   /* cards/containers */
  --purple-tint: #e6e2f8;   /* subtle highlight bands */
}
```

### Typography
- Headings: **Mada**, weights 500/600/700
- Body: **Open Sans**, weights 400/500/600
- Base size: 16px / line-height 1.6
- H1: 32px / 1.2 / Mada 700
- H2: 24px / 1.25 / Mada 600
- H3: 18px / 1.3 / Mada 600
- Small/meta: 13px / 1.4 / Open Sans 500, color `var(--ink-2)`

### Layout grid
- Max content width: **720px** for legal/long-form, **560px** for forms, **480px** for status messages.
- Side padding: 24px desktop / 16px mobile.
- Vertical rhythm: 24px between sections, 16px between paragraphs.
- Border radius: 12px on all cards/containers.
- Shadow: `0 8px 24px rgba(15, 23, 42, 0.08)` on raised cards only.

### Header (shared)
- Sticky top bar, 64px tall, white surface, 1px bottom border `--line`.
- Left: brand wordmark (text logo, Mada 600, 20px, `--push-purple`) linking to the site root.
- Right: optional "Back to site" link, Open Sans 500, 14px.

### Footer (shared)
- Top border `--line`, 32px vertical padding.
- Three stacked rows on mobile / two columns on desktop:
  1. Small copyright line: `© <YEAR> <Site Name>. All rights reserved.`
  2. Inline legal links separated by a 12px dot: Privacy Policy · Terms · CCPA · Contact.
- Text color `--ink-2`, 13px.

### Accessibility
- Minimum body contrast 4.5:1 (use `--ink` on `--surface`).
- Focus state: 2px outline in `--push-purple` with 2px offset.
- Skip-to-content link visible on focus.
- All links underlined inside body copy; remove underline only in nav.
- Tap targets ≥ 44×44px on mobile.

### Responsive breakpoints
- Mobile: ≤ 640px
- Tablet: 641–960px
- Desktop: ≥ 961px



## How to make it cleaner than the original

1. **Strip stock-tool chrome.** The original was built in Unbounce or a similar drag-and-drop tool, so it likely has redundant wrappers, inline styles, and absolute-positioned blocks. Rebuild with a single semantic structure: `<header>`, `<main>`, `<footer>`.
2. **Single typography scale.** Replace the original mixed-font usage with Mada + Open Sans only.
3. **Single color palette.** Replace any off-brand greys/blues with the four-token system above.
4. **Predictable spacing.** Use the rhythm tokens (4 / 8 / 16 / 24 / 32 px) — never one-off margins.
5. **Remove dead weight.** Drop hero image carousels, redundant CTAs, social-proof badges that don't drive action, and trust-icon rows that double up.
6. **One primary CTA per view.** Anything else becomes a secondary text link.
7. **Real semantic HTML.** Headings are `<h1>/<h2>/<h3>`, lists are `<ul>/<ol>`, the form is a `<form>` with `<label>` and proper `name`/`autocomplete` attributes.
8. **Tighter legal copy formatting.** For long-form legal pages, use a sticky in-page TOC and numbered H2s with anchor IDs so users can deep-link to a clause.
9. **Mobile-first build.** Author at 360px first, then progressively enhance to 720/960px.
10. **Performance.** Inline critical CSS (<14kB), defer everything else. Use `font-display: swap`. No external JS unless the page actually needs it.


## Definition of done

- [ ] Every piece of copy from `https://www.prizestash.com/privacy-policy` is present in `index.html` (verbatim for legal sections).
- [ ] Page validates as HTML5 with no console errors.
- [ ] Lighthouse: Performance ≥ 95, Accessibility ≥ 100 on mobile.
- [ ] Renders cleanly at 360 / 768 / 1280 px viewports.
- [ ] All internal legal links (Privacy, Terms, CCPA, Contact) resolve to the matching sibling page in `pages/`.
- [ ] Page uses only the four Pushnami color tokens and the Mada / Open Sans font pair.
