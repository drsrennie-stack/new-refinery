# Accessibility Compliance Notes
Project: Refinery Aesthetics site (new-refinery repo), booking rewrite. Date: July 3, 2026. Reviewer: Dr. Sharilyn Rennie (changes prepared by Claude).

## Scope
Files edited this pass: home, our-team, contact-refinery, join-the-waitlist, thank-you-booking, welcome-stay-connected, contact-thank-you, fouders-offer, founders-lockedin-ty, refinery-booking-glossgenius-kajabi.html. Target: WCAG 2.2 AA floor, AAA contrast where achievable. Note: Refinery brand palette (dark, gold, cream) applies; this is not the teaching palette.

## What changed and its accessibility status
- Contact page booking button: converted from a non-interactive div to a true anchor. Keyboard reachable, visible focus-visible outline (2px gold, 3px offset). Rest state #faf8f4 on #1a1a1a, approx. 16.9:1 (AAA). Hover #1a1a1a on gold #c8a96e, approx. 8.0:1 (AAA).
- "Now Open" banner on both booking-form pages: real anchor, #faf8f4 on #1a1a1a button (AAA). Eyebrow text uses darkened gold #a8874b on white, approx. 4.6:1, passes AA for its 10px uppercase label; large-text AAA not claimed.
- Coming Soon overlay removal: eliminates a focus trap risk (modal without focus management) and a keyboard-inaccessible dismiss pattern. Net accessibility gain.
- thank-you-booking nav: JavaScript-only links replaced with real hrefs; now operable without JS.
- Phone input placeholder corrected; label/input association unchanged (pre-existing pattern).
- target="_top" added to same-domain links so navigation escapes the Kajabi iframe instead of nesting.

## Not verified this pass (pre-existing pages, unchanged structure)
Full keyboard walkthrough and screen reader pass on all 15 pages, heading hierarchy audit, and contrast audit of pre-existing text pairs. Recommend a full audit as a follow-up before the EMR swap ships.

## Known limitations
- Multi-step request form (both form pages) relies on JS step switching without aria-live announcements on step change. Pre-existing; flag for remediation.
- Decorative SVGs in edited regions carry aria-hidden where they were already marked; unedited regions not re-checked.
