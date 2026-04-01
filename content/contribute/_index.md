---
title: Contribute
weight: 10
bookFlatSection: true
---

# Contribute to the Almanac

The Convention City Almanac is an open reference. Entries are credited to their authors.

## What We Need

**City profiles** — Does your city have a convention center? What neighborhood is it in? What was there before? What happened after? We need profiles for convention centers worldwide, using the same structured format.

**Financial research** — Convention center bond documents, audited financials, lodging tax data. We normalize it into comparable formats.

**Urban planning analysis** — Theory entries connecting academic research to convention center placement. Diagnostic vs. prescriptive framing required.

**Local knowledge** — Walk the block. What does the neighborhood around the convention center actually feel like at 7pm on a Tuesday? Photos welcome.

## How to Contribute

**If you use GitHub:** Fork the repository, add your entry in the correct section using the templates below, submit a pull request. Your name stays on the entry.

**If you don't:** Email ivan@conventioncityseattle.com with your contribution. Include sources for every factual claim.

## Entry Templates

### City Profile

Every city entry needs:

```yaml
---
title: "City: Facility Name"
weight: 100           # sort order
date: 2026-04-01      # when you wrote this

# Key metrics
opened: 1988
exhibit_sf: 176480
walk_score: 97
centrality: "in-cbd"  # in-cbd | near-cbd | peripheral | remote
placement: "urban-core"  # urban-core | waterfront | edge-city | greenfield | island

# Context
prior_land_use: "What was on this site before?"
neighborhood_now: "What's the neighborhood like today?"
displacement: false    # Was a community displaced for this facility?

# Sources (every claim needs one)
sources:
  - label: "Wikipedia"
    url: "https://..."
  - label: "City planning document"
    url: "https://..."

tags:
  - convention-center
---

## The Facility
[Size, design, when opened, major renovations]

## What Was Here Before
[Prior land use, displacement history if any]

## What's Here Now
[Current neighborhood character, walkability, transit, retail, housing]

## The Transformation
[What changed because of this facility — or despite it]

## Sources
[Linked list of every document cited]
```

## Standards

- **Every factual claim needs a source.** URL, document title, page number where applicable.
- **Neutral tone.** The almanac describes; it doesn't argue. Save the arguments for the [Dispatch](https://dispatch.conventioncityseattle.com/).
- **Date your entry.** Things change. An entry written in 2026 may need updating in 2027.
- **Acknowledge what you don't know.** "Data not available" is better than a guess.

## Credit

Contributors are credited by name on their entries. If you contribute substantially to the almanac, you'll be listed on the contributors page.

---

*Questions? Email ivan@conventioncityseattle.com*
