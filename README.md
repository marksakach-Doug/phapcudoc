# Kinh Pháp Cú — Bilingual Dhammapada Reader

A small, mobile-friendly web reader for the Dhammapada (423 verses, 26 chapters). Each verse is shown in Vietnamese, with an English translation one tap away for comparison.

Built with AI coding assistance and hand edits.

## Files

| File | Purpose |
|---|---|
| `index.html` | Page structure, styling, and reader logic |
| `verses.json` | All chapter titles and verse text (Vietnamese and English) |

## Run locally

Browsers block loading `verses.json` when you open `index.html` by double-clicking it. Start a local server instead:

```bash
python3 -m http.server
```

Then open <http://localhost:8000>.

## Publish with GitHub Pages

1. Push these files to a GitHub repository.
2. In the repository, go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, and save.

## Data format

```json
{
  "translations": { "vi": "...", "en": "..." },
  "chapters": [
    { "id": "I", "title": "I. Song Yếu", "range": "câu 1–20" }
  ],
  "verses": [
    { "chapter": "I", "number": 1, "vi": "Vietnamese text\nwith \\n line breaks", "en": "English text" }
  ]
}
```

To fix a typo or change wording, edit `verses.json`; no code changes are needed.

## Credits and text sources

- **Vietnamese:** verse translation by HT. Thích Minh Châu. Source: *[add where you got the text]*.
- **English:** F. Max Müller, *The Dhammapada*, in *Sacred Books of the East*, vol. 10 (1881). Public domain.

> **Before making this repository public:** confirm you have permission to republish the Vietnamese text (check the terms on the site you copied it from), or keep the repository private.

## Notes

- The reader remembers your last chapter using your browser's `localStorage`.
- Six adjacent verse pairs (58/59, 87/88, 104/105, 153/154, 195/196, 229/230) show the same English text, which appears to follow Müller's combined renderings.
