# loudoguno-hub

Central repository for public-facing data and content for all [loudog.uno](https://loudog.uno) applications.

## 🎯 Purpose

This repository hosts:
- **Changelogs** - Automated version histories for all apps
- **Roadmaps** - Public development plans and upcoming features
- **Feature Voting** - Community-driven prioritization
- **Documentation** - User guides and public API docs

## 📁 Repository Structure

```
loudoguno-hub/
├── fictionary/         # Fictionary AI app data
├── gen-trivia/         # Gen Trivia app data
└── [app-name]/         # Additional apps...
```

Each app directory contains:
- `changelog/` - Release notes and version history
- `roadmap/` - Public roadmap (if enabled)
- `issues/` - Feature requests and bug reports (if enabled)
- `docs/` - Public documentation (if enabled)

## 🚀 Apps

See [APPS.md](./APPS.md) for a complete directory of all apps.

## 📖 Usage

### Accessing Changelog Data

Changelog data is provided in JSON format for programmatic access:

**Latest version:**
```
https://raw.githubusercontent.com/loudoguno/loudoguno-hub/main/fictionary/changelog/latest.json
```

**Full changelog index:**
```
https://raw.githubusercontent.com/loudoguno/loudoguno-hub/main/fictionary/changelog/index.json
```

**Specific version:**
```
https://raw.githubusercontent.com/loudoguno/loudoguno-hub/main/fictionary/changelog/entries/v1.0.0.json
```

### Data Schemas

All JSON data follows defined schemas in the `schemas/` directory:
- See `schemas/changelog-entry.schema.json` for changelog entry structure
- See `schemas/app.schema.json` for app metadata structure

### Example: Fetch Latest Version

```javascript
// Fetch latest changelog entry for fictionary
const response = await fetch(
  'https://raw.githubusercontent.com/loudoguno/loudoguno-hub/main/fictionary/changelog/latest.json'
);
const data = await response.json();
console.log(`Latest version: ${data.latest.version}`);
```

### Example: Fetch Full Changelog

```javascript
// Fetch complete changelog index
const response = await fetch(
  'https://raw.githubusercontent.com/loudoguno/loudoguno-hub/main/fictionary/changelog/index.json'
);
const data = await response.json();
console.log(`Total releases: ${data.entries.length}`);
```

## 📋 Changelog Entry Format

Each changelog entry (`entries/vX.Y.Z.json`) follows this structure:

```json
{
  "version": "1.4.2",
  "date": "2025-12-01",
  "title": "AI Chat Improvements",
  "summary": "Enhanced AI responses and fixed critical bugs.",
  "build": {
    "sha": "a1b2c3d",
    "num": 123,
    "time": "2025-12-01T17:42:10Z"
  },
  "sections": [
    {
      "emoji": "💎",
      "title": "Improvements",
      "items": [
        {
          "label": "AI Chat",
          "text": "Improved response quality"
        }
      ]
    },
    {
      "emoji": "🐞",
      "title": "Fixes",
      "items": [
        {
          "label": "Multiplayer",
          "text": "Fixed host disconnect crash"
        }
      ]
    }
  ]
}
```

## 🤝 Contributing

This repository is primarily auto-updated by CI/CD pipelines from private app repositories. For:
- **Bug reports**: Visit the specific app's site and use the feedback widget
- **Feature requests**: Coming soon - feature voting system
- **Documentation fixes**: Submit a PR with improvements

## 📜 License

All content in this repository is publicly accessible. Individual apps may have their own licensing.

## 🔗 Links

- Website: [loudog.uno](https://loudog.uno)
- Twitter: [@loudoguno](https://twitter.com/loudoguno)

---

**Note**: This is a public repository. Never commit sensitive information like API keys, secrets, or private data.
