# Wird — support and privacy

The public website for the app **Wird: Daily Quran Habit**, in English and Arabic.

- Home + support + FAQ: https://he-kadry.github.io/wird-site/ (Arabic: /ar/)
- Guide, screen by screen: /guide.html (Arabic: /ar/guide.html)
- Privacy policy: /privacy.html
- Reviewer link page: /review.html (not indexed)

All pages share `style.css` (bump `?v=` in the links after changing it). Screenshots are in `img/`.
This repository holds only these pages; the app source is not here.

## On launch day

- Replace the "Coming soon" App Store button in `index.html` and `ar/index.html` with Apple's official badge (Arabic badge on the Arabic page), linked to the App Store page.
- Reviews: add only real quotes from real readers, with their permission (template in a comment in each page).

## Switching a reciter off (config.json)

The app reads `config.json` at launch and whenever it returns to the
foreground. To withdraw a reciter — for example if a rights holder asks —
edit the file on GitHub (pencil icon → commit) and list its id:

```json
{
  "disabledReciters": ["minshawi"]
}
```

Ids: `husary`, `alafasy`, `minshawi`. The change reaches readers within
about ten minutes (GitHub Pages caching) the next time they open the app:
the reciter disappears from the picker, stops if playing, and its saved
audio is deleted from the phone. Put the list back to `[]` to undo.
Keep the file valid JSON — a broken file is ignored and the last good
setting stays in force.
