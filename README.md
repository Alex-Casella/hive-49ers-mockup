# HIVE Depth Chart: 49ers mockup

A clickable mockup of a clearer team rating and injury view for the HIVE Depth Chart, using the San Francisco 49ers as the example.

**Live page:** https://Alex-Casella.github.io/hive-49ers-mockup/

This is a design mockup for review, not the production app. It runs entirely in the browser from one file (`index.html`), with the 49ers data built in.

## What it shows

**Team rating, explained**
- Full strength → This week (→ With your sit-outs), with exact values under the rounded headline (84.1 → 82.4).
- "Why it changed" lists only the injured players who actually moved the rating, each with their own share. The shares add up to the total, so no single player is shown next to the whole unit's change.
- Injured backups behind a healthy starter are grouped under "No effect" with a reason (for example, "Backup · Odighizuwa starts").
- Your own "what if" sit-outs are a separate step, with Undo per player.

**Injury details, with sources and dates**
- Every fact on a player's sheet shows where it came from: the live injury feed (Sleeper), the NFL's official weekly injury report (via nflverse), or HIVE.
- "On official report since Week X" and a week-by-week strip, so an old injury doesn't look new just because its record was updated recently.
- Old or missing information is labeled: "may be out of date," "not provided by any source," "limited history."
- A coach's decision is shown as "Inactive," not as an injury.

## How to use it

Open the live page on a laptop or desktop browser. It also works at phone width.

Use the **Try** buttons at the top to jump to each example:

| Button | What it demonstrates |
|---|---|
| Bosa | An old injury with a recent update: out every week since Week 3 |
| West | Missing information and no effect on the rating |
| McCaffrey | Newer news than the latest official report |
| Sigle | A status that may be out of date (no update in 9 days) |
| Rourke | A coach's decision, not an injury |
| Sit out Fred Warner | A "what if" sit-out, shown as its own step with Undo |

Other controls in the gold bar:
- **Rating basis:** compare the current rating input with a Madden-only rating.
- **Notes on / off:** show or hide the numbered review notes.

You can also download `index.html` and open it directly in any browser. No install is needed.

## Data

A snapshot from **Mon Nov 2, 2026**:
- **Roster and depth chart:** nflverse, via HIVE (Oct 30).
- **Player ratings:** Madden 27 Week 7 ratings (EA), via HIVE.
- **Injury status, body part, notes and last update:** Sleeper public players API.
- **Official injury reports and practice participation:** nflverse `injuries_2026.csv`, Weeks 1–7.

Team ratings use HIVE's own position weights, so the headline numbers match the app (offense 84 → 82, defense 79 → 78).

## Limitations

- The data is a fixed snapshot. It does not update.
- Some values are fixed for the demo: "Checked by HIVE," the current date, and the 49ers' Week 8 bye.
- Dates are shown in Pacific time.
- When the live feed and the official report disagree on an injury (for example, Mike Evans), the sheet currently shows only the live feed's version.

## Updating the page

Upload a new `index.html` to this repo (Add file → Upload files). The link stays the same, and the page refreshes within a couple of minutes.

---

Built by Alex C. (LUCA). AI (Claude) helped read HIVE's code, compute the ratings and build the mockup.
