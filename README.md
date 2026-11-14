# Game-Shelf

Easy searching boardgames. **Tabletop Shelf** is a single-page board game site built on BoardGameGeek's catalog.

## Features

- **For you**: recommendations from about 4,700 well-rated BGG games, scored on shared mechanics, categories, weight, player count, play time and BGG rating, with a "Because you own…" reason on each pick.
- **Tonight**: pick players, time and weight, and it chooses a game from your own shelf, with alternates and an "Almost" list explaining what doesn't fit.
- **Search**: all 21,645 games in BoardGameGeek's catalog, searchable by name, mechanic or category, with cover thumbnails, player/time/weight filters, and most-rated games first.
- **My shelf**: link your BGG username and import your collection by pasting a BGG CSV export (matched by BGG ID) or a list of game names.
- **Game pages**: cover, players, time, weight, BGG rating and rank, similar games, and "Learn to play" links. Rulebook links open each game's English files on BGG, most recommended first. Eight games link straight to the rulebook file. Every game also has publisher-PDF and how-to-play video links.

## Running it

There's no build step. Turn on GitHub Pages (Settings → Pages → Deploy from branch → `main` / root) to host it at
`https://bilbosagggins.github.io/Game-Shelf/`. Opening `index.html` straight from disk only shows the most popular games, because browsers block loading `games.json` from a local file.

## Data

- `games.json`: the BGG catalog as of January 2022, from the TidyTuesday BoardGameGeek dataset. It adds complexity weights from an older BGG scrape, plus newer games added by hand. Games without a published weight get an estimate, shown with a "~".
- `covers.json`: BGG cover thumbnails, loaded from BoardGameGeek's image server.

## Notes

- Your shelf is saved in your browser's local storage.
- These features only work in the Claude-hosted version, because they use Claude:
  - Ask Claude for picks
  - Teach me in 2 minutes
  - Looking up games newer than the dataset
  - Reading a pasted BGG collection page
