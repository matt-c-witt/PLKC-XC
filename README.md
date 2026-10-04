# PLKC Cross Country

An independent results archive for Kansas City Parochial League (PLKC) cross country,
2017 to present. It is not produced by the PLKC.

The whole site is one file, `index.html`, with the results data built in. There's no
build step, and you can open it directly in a browser.

## What's on the site

- **Seasons:** every meet, with the top three teams and the individual winner in each division.
- **Race results:** the full field for any race, with a chart of every finisher, a team
  scoring chart and a searchable table. Highlight one or two schools.
- **Schools:** every member school with its colors and mascot (taken from each school's own
  website), team finishes over time and its fastest runners.
- **Champions:** City Championship team and individual champions by year, plus team race wins.
- **Records:** the official all-time PLKC records, the top ten on file and course records.
- **Runners:** search any of about 2,300 runners and see their times by course, place in
  every race and personal records.

## How PRs work

A PR only counts against earlier times on the same course at the same distance: St. Pius X,
St. Michael, Missouri Western or JCCC (Border War). The 2021 Border War used a longer
layout and is tracked separately.

## Files

| File | Purpose |
|---|---|
| `index.html` | The site. All results data is built into this file. |
| `netlify.toml` | Serves the folder as-is and keeps browsers from caching an old copy. |
| `DEPLOY.md` | One-time setup and how to publish updates. |
| `CHANGELOG.md` | What changed and when. |
