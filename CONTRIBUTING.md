# Contributing

Thanks for wanting to make The Claude Usecase Map better! This project is meant to grow with the community, and **you don't need to be a developer to help.** There are two easy ways in.

## The easy way: open an Issue

If you have an idea — a task that's missing, a setting that feels wrong, a category that should exist — just open an **Issue**:

1. Click the **Issues** tab at the top of the repo.
2. Click **New issue**.
3. Describe your suggestion. For a new row, it helps to include:
   - the **task** (e.g. "Translate subtitles")
   - the **model** you'd suggest (Opus 4.8 / Sonnet 4.6 / Haiku 4.5)
   - the **effort** (Low / Med / High / Max)
   - **thinking** on or off
   - a one-line **why**

That's it — no code required. Someone can fold it into the file.

## The hands-on way: edit it yourself

All the data lives in one place, so changes are simple.

1. Open `index.html` in the repo and click the **pencil icon** (Edit).
2. Scroll to the `DATA` array near the bottom of the file.
3. Copy an existing line and adjust it. Each row looks like this:

   ```js
   { cat:"Writing", task:"Translate subtitles", model:"Sonnet 4.6", effort:"Low–Med", think:false, why:"Pattern task, light", tags:"subtitles srt translate captions" },
   ```

   - **cat** — the category header it appears under (reuse an existing one to keep grouping tidy).
   - **task** — the short label shown in the list.
   - **model** — `Opus 4.8`, `Sonnet 4.6`, or `Haiku 4.5`.
   - **effort** — `Low`, `Med`, `High`, `Max`, or a range like `Med–High` (the *top* tier sets the colour and cost).
   - **think** — `true` or `false`.
   - **why** — one short reason for the choice.
   - **tags** — invisible search keywords/synonyms so the row is easy to find.

   The cost meter and tooltips update automatically — nothing else to touch.

4. At the bottom, choose **"Create a new branch and start a pull request"**, and describe your change.

A **pull request** (PR) is just a polite "here's a change I'd like to merge" — the repo owner reviews it and clicks merge if it looks good.

## Want your own version instead?

Totally fine — that's the spirit of it. Click **Fork** (top-right of the repo) to get your own copy you can change however you like, host on your own GitHub Pages, and maintain independently. The MIT license explicitly allows this.

## A note on accuracy

The model/effort recommendations are **practical heuristics, not official Anthropic numbers.** When suggesting changes, real-world experience ("I ran this on Sonnet High and it was plenty") is the most valuable input. For anything safety- or correctness-critical, point to the official docs.

## Ground rules

Be kind, assume good faith, and keep suggestions focused on making the map genuinely useful. That's all.
