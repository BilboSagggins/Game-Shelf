# Game-Shelf

Easy searching boardgames. **Tabletop Shelf** is a single-page site that recommends board games based on the games you own.

## Features

- **For you**: recommendations scored on shared mechanics, themes, weight (BoardGameGeek 1–5 complexity), player count and play time, with a "Because you own…" reason on each pick.
- **Search**: about 195 well-known games, searchable by name, mechanic or theme, with player, time and weight filters.
- **My shelf**: link your BoardGameGeek username and import your collection by pasting the copied BGG collection page, the text of a BGG CSV export, or a list of game names.
- **Game pages**: players, time, weight, mechanics, similar games, and a "Learn to play" section. 108 games link straight to their rulebook files on BoardGameGeek; every game links to rulebook PDF searches and how-to-play videos (including Watch It Played).

## Running it

It's one file with no build step. Open `index.html` in a browser, or turn on GitHub Pages
(Settings → Pages → Deploy from branch → `main` / root) to host it at
`https://bilbosagggins.github.io/Game-Shelf/`.

## Notes

- Your shelf and wishlist are saved in your browser's local storage.
- These features work only in the Claude-hosted version of the site, because they use Claude: **Ask Claude for picks**, the **Search every board game** BGG lookup, and turning a pasted BGG collection page into game titles. On a standalone copy:
  - Pasting a CSV export or a plain list of names still works.
  - The BGG search button falls back to a link that searches BoardGameGeek directly.
- Game data (weight, player counts, play time) is approximate and was entered by hand from BoardGameGeek listings.
