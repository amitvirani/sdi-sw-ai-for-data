# AI for Data: Southwest AI Lesson

A 90-minute, hands-on lesson that teaches working professionals to analyze business data with AI: no coding, Claude for analysis, Google Sheets for checking every number.

The instructor leads one dataset on screen (**PhoneHub Mobile**). Then each participant repeats the same steps on their own with a second dataset (**Copper Kettle Coffee**). The prompts are the same and the data is different, so the hands-on shows whether they learned the method, not just the answers.

## Pages

| File | Who it's for | What's in it |
| --- | --- | --- |
| [`index.html`](index.html) | Participants | Downloads, Google Sheets basics, the DATA prompt framework, responsible AI use, guided steps 1–6, hands-on H1–H6, verification log, exit ticket, take-home |
| [`plan.html`](plan.html) | Organizers, trainers | Objectives, run of show, DATA framework, responsible AI, datasets, prep checklist, support for mixed skill levels, grading |
| [`trainer.html`](trainer.html) | Trainer only | Minute-by-minute script (Why / Do / Say / Expect / Watch for), troubleshooting, **full answer keys** |

Each page is a single self-contained HTML file with no build step and no external libraries. Prompts have Copy buttons, and answers sit behind "Show the answer" toggles.

## Data files

All data is **synthetic**: it looks realistic but describes no real customers, staff or sales. The participant page links to these files with download buttons.

| File | Used for | Contents |
| --- | --- | --- |
| [`files/phonehub_sales.xlsx`](files/phonehub_sales.xlsx) | Guided practice | Phone retailer (Atlanta, Denver, Online). Sales 128 rows, Inventory 13, Reviews 40 |
| [`files/copper_kettle_sales.xlsx`](files/copper_kettle_sales.xlsx) | Hands-on | Coffee roaster (Austin, Nashville, Online). Sales 140 rows, Inventory 11, Reviews 30 |
| [`files/phonehub_clean.xlsx`](files/phonehub_clean.xlsx) | Backup + checks | Cleaned PhoneHub data (126 sales rows), personal columns removed |
| [`files/copper_kettle_clean.xlsx`](files/copper_kettle_clean.xlsx) | Backup + checks | Cleaned Copper Kettle data (138 sales rows), personal columns removed |

The raw files contain **planted problems** for participants to find: inconsistent spellings, items filed under the wrong brand or category, a duplicate, blank discounts, wrong totals, out-of-period dates, a price typo (Copper Kettle only), a name mismatch between sheets, and personal details hidden in review text. The trainer guide lists every one, with the exact rows.

The clean files deliberately keep the Inventory name mismatch, so the "check the join" step still works for anyone who restarts from a backup.

## Publishing with GitHub Pages

1. Go to **Settings → Pages** in this repository.
2. Under **Build and deployment**, choose **Deploy from a branch**, branch **`main`**, folder **`/ (root)`**, then **Save**.
3. After a minute the site is live at `https://amitvirani.github.io/sdi-sw-ai-for-data/`. Share that link with participants; it opens the participant page.

The download buttons use relative links (`files/…`), so they work as long as the `files/` folder sits next to `index.html`.

## Before you teach: answer keys are public

This repository is public, so `trainer.html` and the answer keys inside it can be read by anyone who finds them. The participant page doesn't link to the trainer guide. If you want the answers fully private, keep `trainer.html` somewhere else, or make the repository private (GitHub Pages on a private repo needs a paid GitHub plan).

## Tools participants need

- A laptop (not a phone), with a browser
- A Claude account (Pro is ideal; on the free plan, the clean backup files help anyone who hits a usage limit)
- A Google account for Google Sheets
- Optional: ChatGPT or Gemini for a second opinion

## Updating the pages

Edit the HTML directly. Shared styles live in each file's `<style>` block, and they match the Southwest AI site style used in the [Writing with AI](https://asifakberali.github.io/southwest-ai/session-02/activities.html) lesson. If you change a dataset, update the answer keys in `trainer.html` and the "Show the answer" sections in `index.html` to match.
