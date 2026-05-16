# Tafseer-Index

Master manifest for the multi-language Quran tafseer mirror used by the
Mushaf mobile app.

The mobile app fetches `languages.json` from this repo (via jsDelivr) on
first launch to discover:

- What languages have available tafseers
- For each tafseer: its repo, slug, and the URL pattern for the 30 per-juz
  JSON files

## CDN URLs

```
https://cdn.jsdelivr.net/gh/manaf/Tafseer-Index@main/languages.json
https://raw.githubusercontent.com/manaf/Tafseer-Index/main/languages.json
```

## Source

Tafseer data is mirrored from [Quranic Universal Library
(QUL)](https://qul.tarteel.ai) by Tarteel AI. All QUL data is licensed
under their terms — see qul.tarteel.ai/about for attribution.

## Updating

Re-run the import scripts in the Mushaf mobile app:

```bash
python3 scripts/tafseer/pull_qul.py        # pull new/updated tafseer data
python3 scripts/tafseer/build_manifest.py  # rebuild this file
```
