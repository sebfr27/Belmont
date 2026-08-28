# Handoff — where this stands and what's next

## Where things stand

`WEBSITE_PLAN.md` and `BUSINESS_PLAN.md` are written and merged to `main`. Nothing else exists yet — no code, no data file, no images. This doc is the bridge between "plan is settled" and "start building."

Per the plan: build one Flask mockup (homepage, two flagship property pages — Bathgate Houses and Lorillard Houses — plus a mocked availability/pricing page), stop at that fixed checklist, then use it to approach Belmont about an ongoing marketing retainer, not a one-time sale.

## Next steps, in build order

1. **`buildings.yaml`** — real names/addresses for the two flagship buildings and the other five, plus invented unit/price data. This is the first thing to build because every page reads from it.
2. **Homepage + layout shell**, mobile-first.
3. **Two flagship property pages**, new copy, placeholder-labeled unit imagery.
4. **Availability/pricing page.**
5. **Original exterior/neighborhood photography pass** — shot with the X100VI, dropped in.
6. **Responsive QA + contact section.**

I can start on step 1 as soon as the questions below are resolved — some of them block step 1 directly (the data file needs real addresses and *some* number to put in the price fields), others just avoid rework later.

## Questions I actually need answered before or during the build

**Blocks step 1 (the data file):**
- I don't have verified exact addresses, unit counts, or bedroom configs for Bathgate Houses or Lorillard Houses — direct access to belmontstudenthousing.com is network-blocked in this environment, so what I have is secondhand (search-indexed snippets describing "large and small suites," "large suites for 4-5 occupants"). Can you get me the exact addresses and a rough unit breakdown per building — either by sending me what's on the current site, or telling me it's fine to keep placeholders that are clearly approximate?
- For the invented prices on the availability page: should they be grounded in real Bronx/Fordham-area comps (roughly $700-1,500/month per the market research, scaled by unit size), or does it not matter since the numbers are illustrative either way?

**Affects steps 2-3 (visual direction):**
- Belmont's current site has no visible logo/wordmark — do you want me to design a simple text-based wordmark as part of this, or keep the redesign brand-neutral (Belmont's name in a clean type treatment, no invented logo)?
- For unit interiors (out of scope to fabricate as real photos, per the plan): stock photography, a simple illustrated/placeholder treatment, or literal "photos available on request" blocks? This is a real visual-quality tradeoff worth deciding once, not per-page.

**Affects step 5 (photography) and overall timing:**
- Any idea when you can realistically get out to Belmont Ave to shoot exteriors? Steps 1-4 don't depend on it, but I don't want the whole thing stalling on a photo shoot if your schedule is tight this week — happy to launch with a placeholder exterior and swap in real shots later.

**Affects the handoff-to-outreach step (not blocking the build, but worth deciding now):**
- Where should this actually be hosted once it's built? The plan says Render/Fly.io/PythonAnywhere — any preference, or should I just pick one and get a live link you can send?
- Do you want a plain subdomain/project name for the link (e.g. something clearly yours, not looking like an official Belmont property), so it's unambiguous to Belmont that this is a pitch, not a hack of their real site?

None of these block me from starting on the plan structurally — I can scaffold the Flask app and `buildings.yaml` with clearly-marked placeholders right now if you'd rather I start than wait on answers. Say the word either way.
