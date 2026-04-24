# Mirror Box launch-readiness (dogfood for launch-ready v1.0.4)

**Target:** [aihxp/mirror-box v1.0.0](https://github.com/aihxp/mirror-box)
**Mode:** 0 (detect): N/A declaration
**Verdict:** launch-ready does not apply to Mirror Box.
**Version:** 1.0
**Last updated:** 2026-04-23
**Owner:** h (dogfood)

## What this is

launch-ready's Step 0 (mode detection) run against Mirror Box. The detection concludes that launch-ready is out of scope for this target and this document formalizes the N/A with reason.

Purpose: close the launch-ready half of the Mirror Box executional gap from the suite VALIDATION report. Six skills needed dogfood artifacts against Mirror Box; this is the sixth and final.

## Why N/A

launch-ready owns bringing a deployed, healthy app to real users: landing pages, waitlists, launch sequencing, post-launch telemetry, on-day comms. Mirror Box fails three of the four launch-ready gating questions.

### Gating question 1: Is there a product being launched?

**No.** Mirror Box is a tiny traced HTTP echo service used as a teaching target for OTel, SLO authorship, and incident-response practice. It is not a product with customers, revenue, or market positioning. The PRD target-user section explicitly frames it as "observability educators and self-directed learners" using the service as infrastructure for learning, not as something being sold or promoted.

### Gating question 2: Is there a launch-moment to execute against?

**No.** The ROADMAP's M1 ships the service; there is no "launch day," no "D-calendar," no "Product Hunt post," no "Show HN thread." The product goes from "shipped as a reference implementation" to "referenced by workshop curricula" as reuse demand emerges. That is a different shape than a launch.

### Gating question 3: Is there a landing page to build?

**No.** Mirror Box's README is its landing page: what it is, how to run it, how to deploy it, what's out of scope. A marketing-style landing page (hero, social proof, feature grid, CTA, pricing) would be off-brand for a reference implementation and would mislead readers into thinking Mirror Box is a product.

### Gating question 4: Is there a waitlist or signup funnel?

**No.** The PRD's success criteria include no signup funnel, no email capture, no waitlist. Mirror Box's leading KPI is "time-to-first-trace under 10 min from clone," which is a developer-tool metric, not a marketing metric.

## Launch-ready scope fence (self-check)

From launch-ready's SKILL.md "When this skill does NOT apply":

> - **Internal tools, reference implementations, or teaching targets.** launch-ready owns bringing something to real users as a launch-moment event. A reference implementation is used, not launched.

Mirror Box is the canonical match for this scope-fence clause. launch-ready correctly routes to N/A.

## What Mirror Box gets instead (without launch-ready)

Mirror Box does need visibility to serve its purpose. The artifacts that satisfy that need without a launch-ready pass:

- **README as landing.** The README explains what Mirror Box is, who it's for, how to use it, and what's out of scope. That's enough for a reference implementation.
- **Suite-map inclusion.** When the Mirror Box entry is added to the suite's SUITE.md (a followup suite patch), anyone browsing the ready-suite finds Mirror Box through the map.
- **Cross-link from planning-tier dogfoods.** prd-ready, architecture-ready, and roadmap-ready's Mirror Box dogfood artifacts all link to aihxp/mirror-box. Anyone reading those finds the implementation.
- **Honeycomb sample queries.** Once observe-ready's dogfood Tier 2 is wired, the Honeycomb dataset becomes a sharable artifact for workshop participants.

None of those require launch-ready's discipline. Launch-ready is correctly out of scope.

## When launch-ready would apply

If Mirror Box ever graduates:

- **Path A: paid teaching product.** Mirror Box becomes the backbone of a paid workshop series. A landing page with pricing, a waitlist, a launch moment, post-launch conversion funnel all become real work. **launch-ready applies.**
- **Path B: educator platform.** Mirror Box gets a multi-tenant shell, user accounts, saved queries, shared dashboards. Becomes a SaaS. **launch-ready applies.**
- **Path C: renamed reference with a public sponsor.** Mirror Box gets a corporate sponsor (Honeycomb, Fly, etc.) who wants a coordinated announcement. **launch-ready applies.**

None of those are in the PRD. The PRD explicitly declares Mirror Box as a teaching target, not a product. If a maintainer changes the PRD to any of the three paths, re-run launch-ready's Step 0 detection.

## Contrast: Mirror Box's Show-HN-not-launch posture

Mirror Box can appear on Hacker News or dev.to as a "Show HN: tiny traced Node service for OTel workshops" post without that being a launch-ready event. A Show HN post is a share-moment for a free reference implementation, and:

- The README is the landing.
- No waitlist, no OG card work, no conversion funnel, no post-launch telemetry beyond the usual Honeycomb view.
- The "launch" is "I clicked Submit on news.ycombinator.com."

launch-ready correctly does not gate-keep that. The skill's scope is launches that need discipline (landing page anatomy, SEO, waitlist funnel, telemetry). A link-share-to-HN doesn't.

If Mirror Box's share-moment produces viral spikes that exceed the PRD's 50 req/s ceiling, that's an observe-ready concern (alert fires, operator resizes Fly VM), not a launch-ready concern.

## Handoff (back to the suite)

This dogfood records launch-ready's correct N/A routing for Mirror Box. No downstream re-runs. No new inputs to any sibling.

If Mirror Box graduates to a product (paths A, B, or C above), the PRD changes, roadmap-ready adds a launch milestone, and launch-ready re-runs from Step 0 with the non-N/A path. Until then, this document stands.

Ready-suite version table and SUITE.md are unchanged by this commit.
