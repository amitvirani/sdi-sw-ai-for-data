# AI for Data: Southwest AI Lesson

A 90-minute, hands-on lesson that teaches working professionals to analyze business data with AI: no coding, Claude for analysis, Google Sheets for checking every number.

The lesson is built on **the six steps of any analysis**: understand the data, clean it, answer the question, chart it, read the comments, report. The instructor demonstrates each step on one dataset (**PhoneHub**, a phone store). Then each participant does the same six steps on their own with a second dataset (**Corner Café**, a coffee shop). The data is different, so the hands-on shows whether they learned the method, not just the answers.

## Pages

| File | Who it's for | What's in it |
| --- | --- | --- |
| [`index.html`](index.html) | Participants | Downloads, Google Sheets basics, the six steps, how to ask AI, the six PhoneHub demos with labeled prompts, hands-on H1–H6 on Corner Café, a checks log, using AI responsibly, exit ticket, take-home |
| [`plan.html`](plan.html) | Organizers, trainers | Objectives, the six steps, slide-by-slide run of show, how to ask AI, responsible AI, datasets, prep checklist, mixed-ability support, grading |
| [`trainer.html`](trainer.html) | Trainer only | Slide-by-slide script (Why / Do / Say / Expect / Watch for), troubleshooting, **full answer keys** and model prompts |

Each page is a single self-contained HTML file with no build step and no external libraries. Prompts are labeled with their parts (Role, Task, Context, Constraints; or Context, Role, Action, Format, Tone for the report) and have Copy buttons that copy the prompt without the labels. Answers sit behind "Show the answer" toggles.

## Data files

All data is **made up**: it looks realistic but describes no real customers, staff or sales. The participant page links to these files with download buttons.

| File | Used for | Contents |
| --- | --- | --- |
| [`files/phonehub_sales.xlsx`](files/phonehub_sales.xlsx) | Demos | Phone store (Atlanta, Denver, Online). Sales 128 rows, Inventory 13, Reviews 40 |
| [`files/corner_cafe_sales.xlsx`](files/corner_cafe_sales.xlsx) | Hands-on | Coffee shop (Austin, Nashville, Online). Sales 140 rows, Inventory 11, Reviews 30 |
| [`files/phonehub_clean.xlsx`](files/phonehub_clean.xlsx) | Backup + checks | Cleaned PhoneHub data (126 sales rows), personal columns removed |
| [`files/corner_cafe_clean.xlsx`](files/corner_cafe_clean.xlsx) | Backup + checks | Cleaned Corner Café data (138 sales rows), personal columns removed |
| [`files/ai_for_data_class_slides.pdf`](files/ai_for_data_class_slides.pdf) | Participants | The 25 class slides as a PDF (no speaker notes; slide 7's answer panel left out). Linked from the participant page |
| [`files/monthly_sales_example.xlsx`](files/monthly_sales_example.xlsx) | Slide 7 activity | A separate example, not PhoneHub data: 12 months of 2025 sales with July typed as $950,000, plus an About tab with the AI's answer and checks |

The raw files contain **planted problems** for participants to find: inconsistent spellings, items filed under the wrong brand or category, a duplicate, blank discounts, wrong totals, out-of-period dates, a price outlier (Corner Café only), a name mismatch between sheets, and personal details hidden in review text. The trainer guide lists every one, with the exact rows.

The clean files deliberately keep the Inventory name mismatch, so the name-matching check still works for anyone who restarts from a backup.

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

## Updating the pages

Edit the HTML directly. Shared styles live in each file's `<style>` block, and they match the Southwest AI site style used in the [Writing with AI](https://asifakberali.github.io/southwest-ai/session-02/activities.html) lesson. If you change a dataset, update the answer keys in `trainer.html` and the "Show the answer" sections in `index.html` to match. Slide numbers in `plan.html` and `trainer.html` follow the 25-slide class deck.
