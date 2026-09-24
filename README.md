# Kinh Pháp Cú — Bilingual Dhammapada Reader

A small, mobile-friendly web reader for the Dhammapada (423 verses, 26 chapters). Each verse is shown in Vietnamese, with an English translation one tap away for comparison.

Built with AI coding assistance and hand edits.

## Files

| File | Purpose |
|---|---|
| `index.html` | Page structure, styling, and reader logic |
| `verses.json` | All chapter titles and verse text (Vietnamese and English) |

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

- **Vietnamese:** verse translation by HT. Thích Minh Châu. Source: https://phatgiaoaluoi.com/news/Tu-hoc/Kinh-Phap-Cu-Ban-dich-cua-HT-Thich-Minh-Chau-5554/
- **English:** F. Max Müller, *The Dhammapada*, in *Sacred Books of the East*, vol. 10 (1881). Public domain.


## Notes

- The reader remembers your last chapter using your browser's `localStorage`.
- Six adjacent verse pairs (58/59, 87/88, 104/105, 153/154, 195/196, 229/230) show the same English text, which appears to follow Müller's combined renderings.
