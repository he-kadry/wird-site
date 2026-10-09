# Wird — support and privacy

The public support page and privacy policy for the iPhone app **Wird: Daily Quran Habit**.

- Support: https://he-kadry.github.io/wird-site/
- Privacy policy: https://he-kadry.github.io/wird-site/privacy.html

This repository holds only these pages; the app source is not here.

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
