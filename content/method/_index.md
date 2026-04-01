---
title: Method
weight: 11
bookFlatSection: true
---

# Method

## CommonScore Methodology

The [CommonScore](/commonscore/) measures city-wide participation space across 16 dimensions. For each dimension:

1. **Availability** (0.0–1.0): What fraction of weeks per year can you participate?
2. **Scale** (0.0–1.0): How much participation capacity exists, relative to what a major facility could provide?
3. **Score** = editorial weight × availability × scale

Weights sum to 100. A perfect score means every dimension offers participation space every week at convention-center scale. The [full methodology](/commonscore/) documents the formula, weights, calibration benchmarks, and the participation vs. consumption distinction.

## Sourcing Standards

The almanac follows a hierarchy of sources:

1. **Primary documents** — Audited financial statements, bond official statements ([EMMA](https://emma.msrb.org/)), legislation, public records, official websites
2. **Authoritative statements** — CEO/CFO public statements with date and venue, board meeting minutes, rating agency reports
3. **Journalistic sources** — Named reporter, named publication, date, direct quotes
4. **Derived figures** — Calculations from primary sources, work shown

Claims that can't be sourced are italicized as unverified or excluded.

## Scoring Calibration

Scores are calibrated against established data points:

- **Oodi gaming room** (Helsinki): Avail 1.0, Scale 0.2 — purpose-built, daily, free
- **Phoenix Comics** (Seattle): Avail 1.0, Scale 0.1 — nightly organized play, retail-scale
- **Pike Place Market** (Seattle): Avail 1.0, Scale 0.7 — daily vendor participation at institutional scale
- **Singapore hawker centres**: Avail 1.0, Scale 0.7 — 122 centres, UNESCO heritage, vendor-operated

New city scores are normalized against these benchmarks. If a city's maker space scores higher than MassRobotics (Boston), the estimate needs justification.

## Known Limitations

**City-wide scope flattens geography.** A city where participation infrastructure is concentrated in one neighborhood and absent from others gets the same score as one with even distribution. Cape Town's profile discusses this directly.

**Consumption/participation boundary is editorial.** Is noraebang (karaoke) participation or consumption? We say participation — you sing. Is attending a convention participation? We say yes for Industry Networking — you network, you demo, you present. Reasonable people can draw the line differently.

**Scores are estimates, not measurements.** Availability and scale are assessed from research, not measured with sensors. Field verification improves accuracy. Italicized claims are unverified.

**Convention center economic impact figures are almost always overstated.** The almanac cites them as reported but flags the methodology when known. See Heywood Sanders, *Convention Center Follies* (2014) for the academic critique.

## Updates

Entries carry `date` and `lastmod` fields. All previous versions are preserved in [git](https://github.com/ivantohelpyou/convention-city-almanac). The `./generate` script rebuilds the leaderboard and city rankings from score data in city pages.

---

*The almanac is maintained by [Ivan Schneider](https://conventioncityseattle.com/).*
