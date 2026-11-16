# Nur Musik – Design

## Idea in one sentence
Like an old iPod: one list per screen, tap a row to go deeper, tap "back" to go up. The only thing on the screen is music.

## Guiding principles (ADHD-friendly)
1. **One thing per screen.** Each screen is either a list or the "Läuft" (now playing) screen. Nothing else is next to it.
2. **Always the same place for the same thing.** Back is always top left, the screen title is always top center, the current song is always at the bottom.
3. **Nothing moves unless you touch it.** No autoplay, no blinking, no pop-ups except short status messages. The only moving thing is the progress bar.
4. **Few choices.** No feeds, no suggestions, no counters, no badges.
5. **Text over symbols.** Where a symbol isn't immediately obvious, use a word (e.g. "Zufall: An" instead of a shuffle icon).
6. **Large tap targets.** Every row and button is at least 48 px high.

## Colors
Four colors only. Blue is the single accent and always means "selected / active / this is playing".

| Role | Color | Used for |
|---|---|---|
| Background | White `#FFFFFF` | All screens |
| Light grey | `#F2F2F2` | Title bar, bottom bar, pressed row, separators `#E5E5E5` |
| Mid grey | `#8E8E93` | Secondary text (artist, duration), inactive controls |
| Black | `#000000` (text `#111111`) | Titles, main text, icons |
| Blue | `#0A64D6` | Pressed/selected row (white text on blue, like the iPod highlight bar), progress bar, the song that's playing, "Abspielen" button |

- Light mode only, like the iPod. (Open question below.)
- No gradients, no shadows, no transparency effects.

## Typography
- System font (San Francisco on the iPhone).
- Screen title: 17 px, semibold, centered.
- List rows: 17 px regular, black. Second line: 14 px, mid grey.
- Now playing: song title 20 px semibold, artist and album 16 px mid grey.
- Only these sizes, nothing bigger, nothing in capitals.

## Structure: the iPod menu instead of tabs
The bottom tab bar is removed. The start screen is a menu, like the iPod's main menu:

```
┌──────────────────────────────┐
│          Nur Musik           │  title bar (light grey)
├──────────────────────────────┤
│ Playlists                  › │
│ Künstler                   › │
│ Alben                      › │
│ Songs                      › │  ← pressed row turns blue, text white
│ Suche                      › │
│ Läuft                      › │  (only when something is playing)
│ Einstellungen              › │
├──────────────────────────────┤
│ ▶  Song title – Artist     › │  bottom bar: current song
└──────────────────────────────┘
```

- Every row ends with a `›` so you know it leads deeper.
- Back button: `‹ Menü` (or the name of the previous screen), top left.
- The "⋯" menu becomes the "Einstellungen" (settings) entry: device, open Spotify, log out, change Client ID.

## Lists
- Text-only rows: title, and in grey below it the artist or "12 Songs".
- **No cover images in lists.** Covers are colorful and break the four-color rule; the iPod lists didn't have them either.
- Song rows inside an album show the track number in grey on the left.
- The song that's playing has a small blue dot on the left and blue text.
- Top of a playlist/album/artist screen: name, one grey line of info, then two text buttons: **Abspielen** (blue) and **Zufall** (grey outline).
- "Mehr laden" (load more) becomes a normal row at the end of the list.

## "Läuft" (now playing) screen
Like the iPod's Now Playing screen:

```
┌──────────────────────────────┐
│ ‹ Zurück        Läuft        │
├──────────────────────────────┤
│                              │
│        ┌────────────┐        │
│        │   cover    │        │  the only image in the app
│        └────────────┘        │
│                              │
│  Song title                  │
│  Artist                      │  grey
│  Album                       │  grey
│                              │
│  1:12 ━━━━━━━━──────── -2:31 │  blue progress
│                              │
│      ⏮       ▶︎/❚❚      ⏭     │  simple black icons
│                              │
│  Zufall: Aus   Wiederh.: Aus │  text toggles, blue when on
│  Spielt auf: iPhone        › │
└──────────────────────────────┘
```

- Play/previous/next as simple solid black icons (drawn in code, not emojis).
- No "3 von 12": Spotify doesn't report the position of the song in the playlist.
- Shuffle and repeat as text toggles, because the symbols are easy to confuse.
- The cover is the official cover in color. It's the only image in the app.

## Bottom bar (current song)
- One line: play/pause icon, "Song title – Artist", next-song icon (kept from the old mini player).
- Light grey background, thin blue progress line on top.
- Tap the text → "Läuft" screen. Tap the icon → play/pause.

## Motion
- Going deeper: the new screen slides in from the right (200 ms), back slides out to the right. Exactly like the iPod.
- "Läuft" slides up from the bottom.
- No other animations. If the iPhone has "Reduce Motion" turned on, screens just switch without sliding.

## Messages
- Short messages appear at the bottom as a black bar with white text. A link in it (e.g. "Spotify öffnen") is white, bold and underlined (blue on black is hard to read).
- They disappear by themselves. No icons, no exclamation marks.

## What is removed
- All emojis (tab icons ♫ ♥ ◉ ☺ ⌕, 🔀 🔁 🔂, 🔈, 📱 💻).
- The orange accent and the dark theme.
- Gradients and shadows on the player.
- The tab bar.
- Cover images in lists.

## Decisions
1. Light mode only.
2. The cover on the "Läuft" screen is the official cover in color.
3. No click wheel, simple buttons.
4. The start screen is the menu. The app no longer reopens the last tab.
