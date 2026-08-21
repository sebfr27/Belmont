# Belmont Realty spec redesign — project plan

## Why this exists

Belmont Realty (belmontstudenthousing.com) is a 1984-founded, family-run student housing landlord serving Fordham University, run by Dr. Pasquale Perretta. The site is functional but stale: 2015-era property photos, a properties page last touched in 2021, no pricing or availability shown anywhere, and a paper/mail-in reservation process ($600 refundable deposit per person, mailed to a PO Box). Meanwhile the underlying product is genuinely good — furnished units, free maid service, utilities included, walking distance to campus — none of which the site actually sells.

This is not a client engagement. It's an unpaid, self-directed spec project: build a redesign example once, well, and use it to open a conversation with Belmont about hiring me as their ongoing marketing person. See `BUSINESS_PLAN.md` for how the outreach and ask are framed.

## Competitive gap, specifically

Checked against three direct competitors serving the same Fordham-adjacent market:

- **RHAMCO / fordhamoffcampus.com** — has a live `/availability` page and per-property "apply online" flow. Belmont has neither.
- **The Arabella** — has floor-plan-level detail, an availability page, an FAQ page, and active move-in offers. Belmont shows one photo and an address per building, nothing else.
- **BlueSky Living** — has per-building pages with concrete unit features and an active blog for SEO. Belmont's content hasn't functionally changed since 2021.

The common thread: every competitor solves at least one of *live pricing/availability*, *self-service application*, or *active content marketing*. Belmont solves none of the three. That's the specific, provable gap this redesign targets — not "the site looks old."

## Scope — in (v1)

- **Redesigned homepage** — modern layout, copy that actually sells furnished/maid-service/utilities-included/walk-to-campus instead of leaving it buried in prose.
- **Two flagship property pages rebuilt in depth** — Bathgate Houses and Lorillard Houses (both have existing named pages on the current site, giving a clean before/after to show).
- **A mocked availability/pricing page** — invented unit counts and prices, real building names/addresses. This is the single highest-leverage page: it's the exact functional gap every competitor has closed and Belmont hasn't.
- **A copy pass** across all rebuilt pages that surfaces the value props Belmont already has and doesn't sell: furnished, free maid service (alternate weeks), utilities included, walk to campus, the 1984/ex-Fordham-faculty founder story.
- **Mobile-responsive layout** throughout — every competitor site is responsive; there's no evidence Belmont's current WPBakery build is.
- **A styled contact/inquiry section** — a `mailto:` link or a static form is enough; no working backend required for v1.

## Scope — out (v1), and why

- **The reputation/legal history is out of scope for the design itself.** Public reviews surfaced a DA consumer-fraud finding (double security deposits, 2014), a reported 14-month unaddressed mice complaint, and disputed deposit returns. This redesign is a presentation/UX exercise, not an attempt to paper over or fix that — deliberately not engineered around it.
- **Bilingual (EN/ES) content** is not built in v1. Belmont's neighborhood is heavily Spanish-speaking, and this is a real future differentiator worth naming in outreach — but it's not part of the audition piece.
- **No real backend.** No database, no payment processing, no resident portal, no working online application. This is a presentation piece, not a product.
- **No fabricated interior photography of specific units.** I've never been inside a real Belmont unit and I'm not a client — presenting invented "photos" of a specific real unit would be materially misleading in a way invented pricing numbers aren't. Any unit interior shown is a clearly-labeled placeholder/sample. Real photography in scope: exterior, streetscape, and neighborhood shots around Belmont Ave that I can actually shoot myself.
- **Not all 7 properties rebuilt.** Two flagship pages proves the pattern. The other five stay at name/address/photo level in a shared "more properties" section — which honestly demonstrates "here's what I'd do at scale," rather than pretending the whole site is done.

## Definition of done

Ship when the checklist above is fully built, styled, and responsive — **not on a calendar date.** If there's a pull to keep polishing past this list, that's the signal to stop and move to outreach, not a reason to add scope.

## Tech stack

**Flask + Jinja templates, with property/unit data in a single YAML or JSON file** — not a database. Deployed as a small Flask app (Render, Fly.io free tier, or PythonAnywhere).

Why: Flask is already a known tool, so there's no new stack to learn for a portfolio piece. Keeping building/unit data in a data file instead of hardcoded into templates means the mockup and a future "real" site share the same architecture — swapping the data file for a real form/DB later is additive, not a rewrite.

## Suggested build order

Not week-scheduled — the feature checklist is the actual boundary, not a date. Rough hour estimates below are a sanity check against ~5hrs/week during a semester, not a deadline to enforce.

1. **Content/data pass** — `buildings.yaml` with real names/addresses, invented unit/price data for the two flagship buildings, plus the "more properties" list for the other five. (~2-3 hrs)
2. **Homepage + nav/layout shell**, mobile-first. (~4-5 hrs)
3. **Two flagship property pages** with new copy and placeholder-labeled unit imagery. (~4-5 hrs)
4. **Availability/pricing page.** (~3-4 hrs)
5. **Original exterior/neighborhood photography pass** — shoot and drop in. (~2-3 hrs shooting + editing)
6. **Responsive QA pass + contact section.** (~2 hrs)

Total: roughly 18-22 hours — about 4-5 weeks at 5hrs/week if the checklist is respected as the actual scope boundary.
