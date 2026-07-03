# Refinery Booking Audit and Rewrite
Date: July 3, 2026. Repo: drsrennie-stack/new-refinery. All 15 pages audited.

## The core problem found
Every Book button on the home page pointed to /booking, which is the old waitlist page with the "Opening Summer 2026" overlay. The real booking page (GlossGenius embed) lives at /refinery-aesthetics-booking. Only Services linked there. Fixed: all 21 booking links across the site now point to /refinery-aesthetics-booking.

## EMR URL swap (DONE, July 3, 2026)
The booking embed now points to Jane: https://refineryaestheticsllc.janeapp.com/. GlossGenius is fully removed from page content. The updated embed is saved under two names: refinery-booking-jane-kajabi.html (use this going forward) and refinery-booking-glossgenius-kajabi.html (same content, kept so nothing referencing the old filename breaks; delete when convenient). Paste the updated embed into the /refinery-aesthetics-booking Kajabi page to go live.

## July 26 urgency copy (added July 3)
Nine pages now carry the line "Appointments begin July 26 and are filling quickly, book now" (phrasing varies slightly by page): home, contact-refinery, join-the-waitlist, thank-you-booking, welcome-stay-connected, contact-thank-you, fouders-offer, founders-lockedin-ty, and the Jane booking embed. On the booking embed, the "Same-week appointments available" chip now reads "Appointments begin July 26" since same-week was not accurate before opening day. After July 26, this copy should be rolled back to evergreen wording.

## Per-file changes
- home: 4 booking links repointed. Fixed an em dash in the hero.
- our-team: 3 "Join the Waitlist" buttons (nav, mobile nav, CTA strip) replaced with Book buttons. They also pointed at the old mykajabi.com domain.
- contact-refinery: dead gray "Reserve a Consultation" button ("available in May") is now a live booking button with hover and focus states.
- join-the-waitlist (live at /booking): Coming Soon overlay removed (HTML, CSS, JS). Added a "Now Open" banner with a Book Instantly Online button above the request form. Form kept as a fallback. Title em dash fixed.
- thank-you-booking: same overlay removal. Its nav Book Now buttons only re-opened the overlay; now they link to booking. Phone field placeholder said "Coming Soon", now fixed.
- welcome-stay-connected: "Opening May 2026" copy and meta tags rewritten to now-open. Book button added above the signup form. Details strip "Opening / May 2026" is now "Status / Now Open".
- contact-thank-you: "opening in May 2026" copy rewritten; primary button is now Book Your Appointment.
- fouders-offer: urgency bar, hero, step 2, and CTA copy rewritten from "when we open" to open-now. Added "Already claimed it? Book your appointment now" link.
- founders-lockedin-ty: waitlist copy rewritten to "doors are open, book now"; primary button is now Book Your Appointment.
- refinery-booking-glossgenius-kajabi.html: nav links repointed, EMR swap markers added.
- All pages: target="_top" added to same-domain links (71 total). Height-sender script added to the two pages missing it.

## To publish
Paste each updated file into its Kajabi page's custom code block (or push if Pages-deployed). The two big ones for taking appointments today: join-the-waitlist (the /booking page) and thank-you-booking.

## Optional cleanup for later
- /booking and /refinery-aesthetics-booking both exist. Consider making /booking redirect to the real booking page in Kajabi so old shared links land right.
- Services has a small unused "coming soon" CSS block (never applied to any service). Harmless, left in place.
- The 4-step request form pages can be retired once the EMR link is live, if you want one booking path only.
