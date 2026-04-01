---
title: CommonScore
weight: 5
bookCollapseSection: true
bookToC: true
---

# CommonScore

A composite metric for whether a city provides **space for people to do things** — not just watch, eat, or attend.

[WalkScore](https://www.walkscore.com/) measures what you can walk to: restaurants, museums, shops. CommonScore measures something WalkScore doesn't — **participation space**. Can you make art here? Can you rehearse? Can you run organized play? Can you prototype a robot? Can you hold a community forum for 200 people at an affordable rate?

A city with Walk Score 98 sits in a great neighborhood. If its CommonScore is 30, the city has meaningful participation infrastructure — libraries with meeting rooms, makerspaces, farmers markets — but still large gaps where convention-scale space sits empty between private events.

The CommonScore is a **gap analysis**. High-scoring dimensions tell you what the city already does well — and what a commons doesn't need to replicate. Zero-scoring dimensions tell you where to invest.

CommonScore measures participation space **city-wide**, not just near the convention center. A makerspace in Nørrebro counts for Copenhagen. The BPL counts for Boston. Oodi counts for Helsinki. Pike Place counts for Seattle. The question is *"does this city provide participation space for this activity?"* — not *"is it near the convention center."* Convention centers are one provider among many; cities that solved the problem elsewhere should not be penalized for intentional separation.

---

## The Question

> If I show up this week wanting to **do** this activity — not watch, not consume, but participate — is there space for me?

That's the core question. Asked 16 times, once per dimension, for each city.

The distinction is between **consumption** and **participation**:

| | Consumption (WalkScore) | Participation (CommonScore) |
|---|---|---|
| **Food** | Eating at a restaurant | Serving a meal — operating a food stall, selling at a farmers market, feeding a crowd |
| **Arts** | Going to an art museum | Having a studio, residency, gallery wall for your work |
| **Music** | Attending a concert | Rehearsing, performing, booking an affordable all-ages venue |
| **Civic** | Reading at a library | Booking a room for 200 people for a candidate forum |
| **Gaming** | Buying games at a shop | Sitting at a table with 20 people for organized play |
| **Makers** | Buying tools at a hardware store | Using a workshop with a table saw and a laser cutter |

Phoenix Comics scores on gaming because you can sit down and *play*. Pike Place scores on markets because vendors *operate* there.

---

## Two Factors

Each dimension is measured on two axes:

### Weekly Availability

The probability that this activity is available in any given week of the year, in or near the convention center district.

| Value | Meaning | Examples |
|---|---|---|
| **1.0** | Every week | Phoenix Comics organized play, Capitol Hill Tool Library |
| **0.5** | Half the year | Seasonal farmers market |
| **0.05** | A few times a year | Convention-scale gaming (PAX + ECCC + GeekGirlCon ≈ 3 weeks) |
| **0.02** | Once a year | PAX West alone (1 week/52) |
| **0.0** | Never | No participation space exists |

This is measurable. Count the operating weeks, divide by 52.

### Scale

How much participation capacity is activated, relative to what a convention center building could provide. Normalized 0.0–1.0.

| Value | Meaning | Examples |
|---|---|---|
| **1.0** | Convention-scale | PAX (70K attendees, full exhibition floor) |
| **0.5** | Institutional | MassRobotics (40K sq ft, 240+ companies), BPL community meeting rooms |
| **0.1** | Retail / proof-of-concept | Phoenix Comics (~20 people at organized play), Capitol Hill Tool Library |
| **0.0** | Nothing | No participation space |

A retail game shop at full capacity still scores 0.1 because it's using 800 sq ft of a dimension that could use 80,000. That's not a criticism of the shop — it's a measure of how much latent capacity the convention center is leaving on the table.

---

## Why These Two Factors

Because **availability and scale fail in opposite directions**, and the convention center model vs. the commons model represent opposite failure modes:

| | Availability | Scale | Product | Problem |
|---|---|---|---|---|
| **PAX West** (convention model) | 0.02 | 1.0 | 0.02 | Massive but 1 week/year |
| **Phoenix Comics** (retail model) | 1.0 | 0.1 | 0.10 | Every night but 20 people |
| **Commons model** (the goal) | 1.0 | 0.5–0.8 | 0.5–0.8 | Daily participation at scale |

The diagnostic value is in identifying *which* factor is the bottleneck — because the policy response is different:

- **Low availability, high scale** (PAX): The demand exists at scale. Increase frequency — the audience is proven.
- **High availability, low scale** (Phoenix): The demand exists daily. Increase space — people show up every night, they just run out of tables.
- **Low availability, low scale**: No local evidence of demand. Look to other cities for cross-city evidence.

---

## The Formula

For each of the 16 dimensions, multiply three numbers: the **editorial weight** (how much this dimension matters), the **weekly availability** (how often can you participate), and the **scale** (how many can participate at once). Sum across all dimensions, divide by total weight, multiply by 100.

{{< katex display >}}
\text{CommonScore} = \frac{\displaystyle\sum_{i=1}^{16} \; w_i \;\times\; A_i \;\times\; S_i}{\displaystyle\sum_{i=1}^{16} \; w_i} \;\times\; 100
{{< /katex >}}

Where {{< katex >}}w{{< /katex >}} is the editorial weight, {{< katex >}}A{{< /katex >}} is weekly availability (0–1), and {{< katex >}}S{{< /katex >}} is scale (0–1).

**A score of 100 means every dimension offers participation space every week at convention-center scale. A score of 0 means the building sits empty between private, catered events** — the current model, where the convention center's calendar is filled with closed-door corporate bookings through an exclusive caterer (Aramark at SCC), not public participation.

---

## Weights

The editorial weights encode a position about what a functioning commons should prioritize. They are published here; you can substitute your own.

| # | Dimension | Weight | Why |
|---|---|---|---|
| 1 | Food & Independent Operators | **11** | Highest-frequency daily need. The convention center's largest revenue line (captive catering) is the commons' largest opportunity (independent operators). |
| 2 | Civic & Community | **11** | The democratic core. Where does a neighborhood choir rehearse? Where do candidates hold forums? |
| 3 | Education & Workforce | **9** | Daily access to learning — not annual conferences about education. |
| 4 | Arts & Studios | **7** | Production space, not exhibition. High ceilings and empty floors are what artists need. |
| 5 | Music & Performance | **7** | Venue crisis is real. Convention centers have acoustically isolated rooms sitting empty. |
| 6 | Makers & Fabrication | **7** | Loading docks and freight elevators have value beyond moving convention freight. |
| 7 | Industry Networking | **7** | Can you meet peers in your field, attend sessions, demo products? This is what convention centers do well. |
| 8 | Markets & Seasonal | **7** | Weekly/seasonal rhythm through large open spaces. Vendor participation, not shopping. |
| 9 | Kids & Families | **6** | $500 vs. $10,000 for a recital hall is the difference between access and exclusion. |
| 10 | Robotics & Innovation | **6** | Proven across [Boston](/cities/boston/massrobotics/), [Pittsburgh](/cities/pittsburgh/cmu-robotics/), [Detroit](/cities/detroit/michigan-central/). |
| 11 | Wellness | **5** | Low-cost, high-need. Shower facilities and quiet rooms already exist in convention centers. |
| 12 | Seniors | **4** | Adjacency programming. In Seattle, Horizon House residents are 3 blocks from the Arch. |
| 13 | Gaming & Organized Play | **4** | Conventions do this well episodically. The commons adds the daily version. |
| 14 | Theater & Film | **4** | Partnership model — overflow and fringe, not replacement. |
| 15 | Sports & Fan Culture | **2** | Arenas exist. The commons adds civic gathering, not spectating. |
| 16 | Mega-Events | **3** | The status quo. Convention centers exist and host large events. |

**Weights sum to 100.**

---

## The Induced Demand Hypothesis

The CommonScore is not just descriptive. It's predictive.

The convention center model assumes demand is **fixed and external**: conventions exist, cities compete to host them. Supply follows demand.

The commons model assumes demand is **latent and local**: people would do robotics, gaming, art, and civic organizing if the space existed at accessible price points. Supply generates demand.

This is the same induced demand argument as highway lanes and bike lanes, applied to public space. And the evidence for it is already in the data:

- **MassRobotics**: Built 40,000 sq ft of robotics workspace. $2B+ in startup funding followed. The demand didn't exist before the space.
- **PAX West**: Started with 3,300 attendees in 2004. Now 70,000+. The event created the audience.
- **Phoenix Comics**: Runs organized play every night because when they put out tables, people sit down.
- **Capitol Hill Tool Library**: Volunteer-run since 2007. Pay-what-you-can. Open 6 days a week. People showed up because the space existed.

The policy question a CommonScore answers is not "how does your city rate?" but **"where should your city invest in participation space?"**

A low score on a dimension with high weekly availability but low scale (proven daily demand, constrained by space) is the strongest signal: **the bottleneck is supply, not demand.** Increase the space and the demand will follow — because it's already showing up every night in 800 square feet.

---

## Interpreting the Score

| Range | Interpretation |
|---|---|
| **60–100** | Commons model in practice — daily participation at scale across most dimensions |
| **40–59** | Strong participation infrastructure exists; convention center still primarily episodic |
| **20–39** | Some participation spaces exist at institutional scale; significant gaps remain |
| **10–19** | Convention center dominates; alternatives are retail-scale proofs-of-concept |
| **0–9** | Single-use event facility with minimal participation space |

---

## What the Score Exposes

A city with **Walk Score 98** and **CommonScore 5** is a city that's great to walk *to* but where you can't *do* anything inside the building most days.

| | WalkScore | CommonScore |
|---|---|---|
| **Measures** | What you can consume nearby | Where you can participate |
| **Question** | Can I walk to a restaurant / museum / shop? | Can I make art / rehearse / prototype / organize here? |
| **Time horizon** | Snapshot | Weekly probability |

They're complementary. WalkScore says the neighborhood works. CommonScore says the building doesn't.

---

## City Scores

### Seattle (Worked Example)

**Walk Score: 98 (downtown). [CommonScore: 27](/cities/seattle/commonscore/).**

The convention center contributes 16% of Seattle's score (Industry Networking + Mega-Events). The other 84% was built by libraries, community centers, markets, makerspaces, music venues, and parks.

Full 16-dimension table with evidence: **[Seattle CommonScore page](/cities/seattle/commonscore/)**.

---

### All City Scores

Full dimension-level scoring tables are on each city's CommonScore page. Full rankings on the **[leaderboard](/commonscore/leaderboard/)**.

Top-level summary (21 cities scored — full rankings on the [leaderboard](/commonscore/leaderboard/)):

| City | CommonScore | The story |
|---|---|---|
| [**New York**](/cities/new-york/commonscore/) | **38** | Three library systems, CUNY, off-off-Broadway. Institutional depth at NYC scale. |
| [**Boston**](/cities/boston/commonscore/) | **32** | University density + MassRobotics. Two convention centers, one rich city. |
| [**Helsinki**](/cities/helsinki/commonscore/) | **30** | The commons exists — it's called Oodi. One building covers 7 dimensions. |
| [**Washington DC**](/cities/dc/commonscore/) | **30** | The capital advantage — civic infrastructure is world-class. MLK Library has a maker space. |
| [**Taipei**](/cities/taipei/commonscore/) | **28** | Night markets as daily cultural institution. Distributed participation. |
| [**Tokyo**](/cities/tokyo/commonscore/) | **28** | Extraordinary participation infrastructure. None of it near Big Sight. |
| [**Seattle**](/cities/seattle/commonscore/) | **27** | Strong distributed infrastructure. No commons building. Convention center contributes 16%. |
| [**Chicago**](/cities/chicago/commonscore/) | **26** | Largest convention center in North America + rich storefront theater tradition. |
| [**Pittsburgh**](/cities/pittsburgh/commonscore/) | **24** | University-anchored robotics model. CMU RIC opened 2026. |
| [**Copenhagen**](/cities/copenhagen/commonscore/) | **23** | Strong Nordic civic culture — just not in Ørestad. |
| [**Vancouver**](/cities/vancouver/commonscore/) | **22** | Municipal community centre model. Crown corp convention centre with civic mandate. |
| [**Detroit**](/cities/detroit/commonscore/) | **20** | Rebuilding after bankruptcy. Strong maker/arts culture, recovering infrastructure. |
| [**Nashville**](/cities/nashville/commonscore/) | **14** | The one city where participation culture is real — but only for music. |

**The highest score is 38. Out of 100.** No city has broken into the 40+ band — "strong participation infrastructure." Helsinki at 30, with Oodi, is the closest a smaller city has come. One purpose-built commons building took Helsinki from ~18 to 30.

**Industry Networking matters.** Convention centers get credit for what they actually do: host professional conferences. McCormick Place scores 5.0 on Industry Networking — the highest in the dataset. This is honest: convention centers are good at industry networking. The CommonScore question is *what else could the building do?*

---

## The Supply-Side Gap Analysis

The CommonScore's policy output is a gap analysis per city. For each dimension, availability and scale diagnose **what's missing**:

| Diagnosis | Availability | Scale | Meaning | Policy response |
|---|---|---|---|---|
| **Proven demand, needs space** | High | Low | People show up every night but run out of tables | Increase supply — demand is demonstrated |
| **Proven scale, needs frequency** | Low | High | Massive when it happens, but only 1 week/year | Increase frequency — the audience is proven |
| **Cross-city evidence** | Low | Low | Nothing here, but other cities prove the model | Build — look to Boston, Pittsburgh, Detroit for precedent |
| **No evidence yet** | Low | Low | No local or cross-city precedent | Untested — but adjacency may justify pilot |

**Seattle examples (city-wide):**

| Dimension | Avail. | Scale | Diagnosis | Evidence |
|---|---|---|---|---|
| Gaming | 1.0 | 0.2 | **Proven demand, needs space** | Phoenix is full every night. Mox Boarding House fills tables. PAX sells out in hours. The bottleneck is square footage. |
| Makers | 0.7 | 0.2 | **Proven demand, needs space** | Capitol Hill Tool Library — volunteer-run, pay-what-you-can, 6 days/week since 2007. The demand is 19 years old. |
| Robotics | 0.2 | 0.2 | **Cross-city evidence** | MassRobotics, CMU RIC, and Michigan Central prove the model. Seattle has no equivalent. |
| Seniors | 0.5 | 0.3 | **Adjacency justifies scale-up** | Horizon House residents 3 blocks from the Arch. Senior centers exist city-wide but none connected to convention center space. |

---

## Transparency

The weights, availability estimates, scale estimates, and evidence for each city are published on this page. The formula is simple enough to recalculate by hand.

If you disagree with the weights — if you think robotics should be weighted 12 and food should be weighted 6 — apply your own weights to the same data and see what happens to the rankings. The editorial position is in the weights. The measurement is in the availability and scale estimates.

If you disagree with the estimates — show us the data. We'll update the score.

---

## Sources & Method

- WalkScore methodology: [walkscore.com/methodology](https://www.walkscore.com/methodology/)
- Seattle Commons vision (16 dimensions): [commons.conventioncityseattle.com/vision](https://commons.conventioncityseattle.com/vision)
- Induced demand in transportation: Duranton & Turner, "The Fundamental Law of Road Congestion" (2011)
- City-level evidence documented in [almanac city profiles](/cities/)

*CommonScore methodology published 2026-04-01. City-wide participation space model. 16 dimensions.*
