\---

name: weekly-update
description: Write a short, plain-language summary of the week's progress. Use this whenever the user asks for a weekly update, a summary of the week, "what did I get done this week", a progress recap, or a status write-up for the past few days, even if they don't say "weekly update" explicitly.
---

# Weekly Update

Produce a short summary of what changed this week, written for the user's own reference. The point is a quick, honest picture of progress that is easy to re-read later, so keep it compact and free of jargon.

## Step 1: Check what changed since the last update

Find the date of the last update first, because "this week" really means "since the last time the user wrote one." Look for it in this order and use whatever is available:

1. **Previous update file.** If the user keeps past updates in a folder (for example files named `weekly-update-\*.md`), read the most recent one. Its date is your starting point, and its contents help you avoid repeating old items.
2. **Git history.** If you are in a git repository, review commits and merged PRs since that date (`git log --since=<date> --oneline`, plus PR titles if available). Read commit messages for intent rather than just counting commits.
3. **Connected apps.** If relevant connectors are available (Gmail, Calendar, Drive and similar), use them for work that doesn't show up in code: documents edited, meetings held, threads concluded.
4. **Ask.** If none of these give you a start date or any changes, ask the user once for the date of the last update and a rough list of what happened.

If there is no previous update at all, default to the last 7 days and say so in the write-up.

## Step 2: Group the changes by category

Sort everything you found into three buckets:

* **Features**: new things that now exist or work.
* **Fixes**: things that were broken and now aren't.
* **Docs**: writing, notes, and documentation added or improved.

Drop noise such as formatting-only commits, merge commits, and duplicates. If something doesn't fit any bucket, fold it into the closest one rather than inventing a fourth. If a bucket is empty, that's fine; note it briefly rather than padding it.

## Step 3: Write it up

Write exactly **three short paragraphs**, in plain language, with no jargon. The user is the only reader, so write the way you'd explain it to them over coffee.

* Paragraph 1: features
* Paragraph 2: fixes
* Paragraph 3: docs

Each paragraph should be two to four sentences. Say what changed and why it matters in everyday words; if a technical term is unavoidable, explain it in a few words. Don't use bullet lists, headers, or commit hashes in the write-up itself.

If a category had nothing, use one sentence saying so (for example, "No documentation changes this week.") so the three-paragraph shape stays consistent.

## Output

Give the three paragraphs in the reply. Mention at the end, in one short line, which period was covered and where the information came from (for example, "Covers Oct 20 to Oct 27, based on git history"). If the user keeps a folder of past updates, offer to save this one there so next week's update has a starting point.

