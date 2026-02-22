# swift_type.

A 15-second typing test website that adapts to your skill level.

![swift_type logo](swifttypefavicon.png)

> **[Try it here](https://aditya-giri-4356.github.io/Swift_type./versions/)** - Pick between v2.0.1 or Classic v1.0.0

## Version
v2.0.1

## What it does

You get 15 seconds. Type as fast and as accurately as you can. The site tracks your speed (WPM) and accuracy in real time, then shows your results when the timer runs out. Press Tab to go again.

The word generation system picks words based on how well you've been doing. It starts simple and ramps up as you get faster. If you keep messing up certain keys, it'll throw more of those at you so you actually improve.

## Features

- **15-second test** with a live countdown timer
- **Real-time WPM and accuracy** displayed as you type
- **Adaptive difficulty** - the words get harder as you get better
- **Weak key targeting** - if you keep mistyping a letter, you'll see it more often
- **Smooth cursor animation** - the cursor slides between characters instead of jumping
- **Three keyboard styles** - round (default), square, or bordered. Toggle in the top-right corner
- **Three-line text display** with smooth scrolling as you type through lines
- **Backspace support** for correcting mistakes
- **Clean results screen** showing final WPM and accuracy when the timer ends

## How difficulty works

The system tracks your last few tests and adjusts what words it gives you:

- **Level 1-2**: Short, common words (the, and, for, run, big, etc.)
- **Level 3-4**: Medium words (about, dance, music, queen, etc.)
- **Level 5**: Longer words (computer, business, analysis, etc.)

If your WPM is above 60 with 95%+ accuracy, difficulty goes up. If you're below 30 WPM or under 80% accuracy, it scales back down. It also tracks which specific keys you make errors on and includes words with those letters more frequently.

## Word generation

All words are generated locally from a built-in corpus of 200+ English words across three difficulty tiers. No external APIs, no network calls, no loading delays. Words are shuffled each time so you don't get the same sequence twice.

## Tech

- HTML, CSS, vanilla JavaScript
- No frameworks, no dependencies, no build step
- Google Fonts (League Spartan, Roboto)

## How to use

1. Open the site
2. Start typing — the timer begins on your first keypress
3. Type the grey text as fast and accurately as you can
4. White = correct, red = wrong
5. Results show up when the timer hits zero
6. Press Tab to restart with fresh words

## Links

**Version selector**: https://aditya-giri-4356.github.io/Swift_type./versions/

**Latest (v2.0.1)**: https://aditya-giri-4356.github.io/Swift_type./

**Classic (v1.0.0)**: https://aditya-giri-4356.github.io/Swift_type./versions/v1.0.0/

## File structure

```
swift_type/
  index.html          (v2.0.1)
  swifttypefavicon.png
  swifttype..png
  README.md
  versions/
    index.html         (version selector)
    v1.0.0/
      index.html
      README.md
      swifttypefavicon.png
```

## Browser support

Works on Chrome, Firefox, Safari, Edge — anything modern with JS enabled. Chrome recommended.

## Setup

Clone the repo and serve it from any web server (or just open `index.html` directly).

## License

MIT

## Changelog

### v2.0.1
- Smooth cursor animation — cursor now slides between characters instead of teleporting
- Replaced external API word fetching with a self-contained corpus of 200+ words
- Loading bar shown before text generation completes
- Cursor properly hides on the results screen
- Removed stray character from HTML
- Cleaned up empty CSS rulesets

### v2.0.0
- Added adaptive difficulty system
- Added performance tracking and weak key detection
- Text generation from multiple internet APIs with smart fallback
- Progressive difficulty scaling
- Updated UI

### v1.0.0
- Initial release
- 15-second typing test
- Dynamic keyboard visualization
- Three keyboard styles
- Real-time WPM and accuracy