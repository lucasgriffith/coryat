# Coryat

Spaced-repetition trivia drills for the buzzer — a single self-contained HTML page,
no build step and no runtime dependencies. Everything (data, maps, flags, logic) is
inlined in `index.html`; progress lives in the visitor's own browser via localStorage.

## Decks

| Deck | Items | Card types |
|---|---|---|
| Countries | 195 | capital, flag, location |
| Physical geography | 100 | where is it, name it from the clue |
| U.S. states | 52 | capital, nickname, location, statehood |
| U.S. presidents | 47 | number, years, VP, home & birthplace |
| World leaders | 172 | name from clue, what and when |
| Historic events | 266 | name the event, year, where |
| Literature | 150 | work, author, characters |
| Shakespeare | 51 | play, characters, quotations |
| Art | 120 | work, artist, movement |
| Classical music | 190 | composer, nationality & era, work, nicknames |
| Mythology | 160 | figure, domain, Greek ↔ Roman |
| Periodic table | 118 | symbol ↔ name, place in the table, lore |
| Pavlovs | 300 | stock reflex pairs |

## Deploy

Static. Vercel needs no build command and no output directory beyond the repo root.

```bash
npx vercel deploy --prod      # from this folder
```

Or connect the repo in the Vercel dashboard — framework preset **Other**, build
command empty, output directory `.`.

## Scheduling

Leitner boxes. A missed card returns later in the same session (never sooner than six
cards, never twice in a row); a correct card moves out to 1, then 3, 7 and 21 days.
Box 4 and up counts as mastered.
