# PLACEHOLDERS — nail-gallery demo (must resolve BEFORE commissioning)

Prospect: **Nail Gallery**, 304 W Evergreen Ave, Ste 104, Palmer, AK 99645 · (907) 745-1311
Repo: `MrJCarrazco/nail-gallery-demo`

> **Call-sheet correction:** an internal call sheet listed this business in **Wasilla**.
> It is in **PALMER**. Every public source agrees on Palmer, AK 99645. Do not open the
> call with "Wasilla".

## VERIFIED — safe to show (sourced, not invented)

| Item | Value on page | Source |
|---|---|---|
| Business name | Nail Gallery | Yelp, MapQuest, BBB, Nextdoor, aggregator page — all agree |
| Address | 304 W Evergreen Ave, Ste 104, Palmer, AK 99645 | Yelp, MapQuest, BBB, Giftly all agree. OSM confirms 304 W Evergreen Ave is a real multi-tenant address in Palmer's central business district |
| Phone | (907) 745-1311 | Yelp, MapQuest, BBB, Nextdoor (`tel:+19077451311`) — all agree |
| Line of business | Nail salon | every listing |
| Services: manicures, pedicures, gel polish | 3 service cards, each marked "Confirmed" | task-verified facts + aggregator "About" copy |
| Google rating | "4.2 · 105 reviews · Google" | task-verified; corroborated by the nailsites aggregator page ("4.2★ · 105 Google reviews") |
| Yelp rating | "4.4 · 25 reviews · Yelp" | Yelp listing title/snippet + MapQuest shows Yelp (25) |
| Nextdoor Fave Awards | "4× Neighborhood Favorite — 2019, 2020, 2023, 2024" | **read verbatim off the Nextdoor page**: "Nail Gallery was a Neighborhood Favorite in 2019, 2020, 2023 and 2024." |
| Map pin | OSM building-level geocode of 304 W Evergreen Ave (61.59912, -149.11892) | Nominatim. Caption states it is building-level and that Ste 104's entrance is not separately mapped |

## PLACEHOLDERS / UNVERIFIED — visible on page as placeholders or omitted

| Item | Status on page | Action before live |
|---|---|---|
| **Opening hours** | **Visible dashed placeholder box** that lists all four conflicting versions and states no hours are published | Owner supplies real hours |
| **Photography** | **Six dashed "YOUR PHOTO HERE" tiles.** Zero photos ship — no stock, no other salon's work | Owner supplies real photos of their own work |
| **Full service menu** | **Visible dashed placeholder box** listing what is still needed | Owner supplies |
| **Pricing** | Not shown anywhere | Owner decides whether to publish |
| **Acrylics / nail art / dip powder** | **Deliberately NOT stated as fact.** The placeholder box notes aggregators list them but that those pages are auto-generated | Owner confirms before any appears as a service |
| **Walk-in policy** | Not stated. The aggregator claims "walk-ins welcome" but it is auto-generated, not the owner's words | Owner confirms |
| **Years in business** | **Deliberately omitted.** Yellowpages shows "24 Years in Business" — single unconfirmed source | Owner states a real founding year |
| **Owner / staff names** | **Deliberately omitted** — none published in any source found | Confirm before any personalisation |
| **Testimonials / review text** | **Deliberately omitted entirely.** Only aggregate scores appear, each with its platform named | Only ever quote a real review, with permission |
| **Logo / brand colours** | Text + hand-coded SVG polish-bottle and almond-nail marks. No logo used (no permission) | Request logo + colours |
| **Email address** | **Deliberately omitted.** The only public email is the Tacoma-domain one, which is dead (see below) | Owner supplies a real address |
| Appointment form | Disabled (JS `alert`) — transmits nothing | Wire `action="https://formsubmit.co/OWNER_EMAIL"` on commission |
| `robots noindex,nofollow` | **ON** | Remove ONLY after commissioning + owner approval |
| Domain | none; demo on github.io | Check availability on commission |

## THE SALES ANGLE — re-verified by hand, with one correction

### Finding 1 — Nextdoor publishes a Tacoma, WA business's web + email: **CONFIRMED**

Read directly off `nextdoor.com/pages/nail-gallery-palmer-ak-1`. The page is
unambiguously this business (Palmer, AK; `tel:+19077451311`; the four Fave Awards)
and it publishes:

- website `gallerynailsspatacoma.com`
- email `webmaster@gallerynailsspatacoma.com`

`gallerynailsspatacoma` is the exact Facebook handle of **Gallery Nails And Spa,
1816 S Mildred St c, Tacoma, WA 98465, (253) 565-2965** — a different nail salon
~1,500 miles away, whose real live site is the differently-spelled
`gallerynailstacoma.com` (resolves to 104.21.33.211, `<title>Gallery Nails And Spa</title>`).

**Corroboration:** MapQuest's Nail Gallery (Palmer) listing *also* publishes
`https://gallerynailsspatacoma.com/` as the business's "Web" link. So the bad data is on
at least **two** directories, not one.

### ⚠ CORRECTION — the domain is DEAD, so do not say "sending customers to a competitor"

`gallerynailsspatacoma.com` **does not resolve.**

| Check | Result |
|---|---|
| Google public DNS, A record | `Status: 3` (NXDOMAIN), no answer |
| Cloudflare public DNS, A record | `Status: 3` (NXDOMAIN), no answer |
| Google public DNS, MX record | `Status: 3` (NXDOMAIN), no answer |
| `curl http(s)://gallerynailsspatacoma.com` | `curl: (6) Could not resolve host` |
| Control: `gallerynailstacoma.com` | resolves fine → proves the resolver works |

**Therefore:** a customer who taps that link gets a **browser error page**, not the Tacoma
salon's website. And `webmaster@gallerynailsspatacoma.com` has **no MX record**, so mail to
it cannot be delivered.

**Say this on the call (true):** "Two directories publish a website and an email address for
you that carry another nail salon's branding — a shop in Tacoma, Washington — and the domain
is dead, so anyone who taps it gets an error page and any email sent there bounces."

**Do NOT say (false):** "your listings are sending your customers to a competitor's website."
They are not; the link is broken. The page copy reflects the accurate version.

### Finding 2 — no website they control: **CONFIRMED**
`nail-gallery-palmer.nailsites.com` renders a full official-looking salon site: hero,
hours, an "About" paragraph, a gallery of 8 photos served from `images.nailtechnetwork.com`,
a four-item service menu (Classic Manicure / Spa Pedicure / Gel Polish Manicure / Acrylic
Full Set) and a **"Reserve online" button pointing at `lacquer.beauty`** — a third-party
booking platform. No claim-this-page or owner-contact path anywhere on it. The service menu
and the booking link were therefore treated as **not the owner's words** and are not stated
as fact on the demo.

### Finding 3 — hours conflict across sources: **CONFIRMED**
- nailsites aggregator: **Mon–Sat 9:00 AM–7:00 PM, Sunday closed**
- Nextdoor: **Mon–Sat 10:00 AM–7:00 PM, Sunday 10:00 AM–5:00 PM**
- third source: **Sunday 9:00 AM–5:00 PM**
- Facebook page "New Nail Gallery" (`facebook.com/gallerynail`): *"Nail gallery under new
  management . we open 7 day/week"*

That last one may be the actual cause of the conflict — a management change would explain
stale hours everywhere. **Worth asking on the call; do not assert it.** Two Facebook pages
exist under this name (`gallery1may2017` and `gallerynail`), which is its own listing problem
worth raising.

## Could NOT verify (explicitly unresolved)
1. **Opening hours** — four conflicting versions; none authoritative.
2. **Whether the business changed management** — one Facebook page says "under new
   management", with no date and no corroboration.
3. **Google rating/review count read first-hand** — 4.2/105 comes from the task brief and the
   aggregator page, not from a direct Google Business Profile read.
4. **Who created the Nextdoor listing**, and therefore whether the business can edit the
   Tacoma web/email fields itself.
5. **Why a Tacoma salon's handle is on a Palmer listing** — data-broker contamination is the
   obvious guess, but the mechanism is unproven.
6. **Whether `gallerynailsspatacoma.com` ever resolved** — it is NXDOMAIN now; no history checked.
7. **Services beyond manicures / pedicures / gel polish** — acrylics, dip, nail art, waxing all
   appear only on auto-generated pages.
8. **Pricing** — nothing published anywhere.
9. **Owner and staff names** — not published.
10. **Years in business** — a single yellowpages "24 Years" with no corroboration.
11. **Walk-in vs appointment policy** — only the auto-generated page claims walk-ins.
12. **Whether the salon knows about or controls the nailsites.com page** or the
    `lacquer.beauty` booking link pointed at it.
13. **Exact suite-104 map pin** — geocode is building-level only.
14. **Which of the two Facebook pages is current/official.**

## No fabricated claims
No testimonials, no review text, no invented ratings, no years in business, no awards beyond
the four Nextdoor Fave Award years printed verbatim on Nextdoor's own page, no staff names, no
invented service items, no prices, no stock photos. Every number on the page is an aggregate
score shown with its platform named.

## Agency identity
Visible agency credit is **"Digital Consulting Studios"** only. No personal human byline
appears anywhere (verified by grep for "Juan" / "Carrazco" / "mrjca" against the served bytes
— 0 / 0 / 0).

## Reduced-motion bug — fixed and verified
The house CSS carries a blanket
`@media (prefers-reduced-motion: reduce){*{animation:none!important;transition:none!important}}`
while 6 hero elements are declared `opacity:0;animation:rise … forwards`. Disabling the
animation leaves them permanently invisible — a blank hero with no headline, no CTA and no
phone number, which is exactly what a phone with Reduce Motion enabled would show.

Fixed with a scoped restoration block, kept **last** in the stylesheet, forcing
`opacity:1!important;transform:none!important` on `.mark`, `.kicker`, `.hero h1`,
`.hero .sub`, `.cta-row`, `.hero .pin` and all `.reveal` variants. Verified on the live URL in
a single active foreground tab with `prefers-reduced-motion: reduce` emulated: **6/6 hero
elements at computed opacity 1 with a non-zero bounding box.**

## Contact rule observed
The business was **not contacted** in any way during this build — no call, email, form, DM,
review or booking request. The appointment form on the page is deliberately inert.
