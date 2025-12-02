# loudog.uno Apps

This repository contains public data for all loudog.uno web applications.

## Active Apps

### Fictionary AI
**Status:** Beta | **First Released:** Dec 2025
- Description: Multiplayer word game where players bluff each other with fake definitions
- URL: https://loudog.uno/fictionary
- [Changelog](./fictionary/changelog) | [Roadmap](./fictionary/roadmap)

### Gen Trivia
**Status:** Beta | **First Released:** Dec 2025
- Description: AI-powered Jeopardy-style trivia game
- URL: https://loudog.uno/gen-trivia
- [Changelog](./gen-trivia/changelog)

## Data Structure

Each app has its own directory containing:
- `changelog/` - Version history and release notes
- `roadmap/` - Public development plans (if enabled)
- `issues/` - Feature voting and bug reports (if enabled)
- `docs/` - User guides and documentation (if enabled)

## Access Patterns

### Changelog URLs

For any app, you can access changelog data at:

```
https://raw.githubusercontent.com/loudoguno/loudoguno-hub/main/{app-slug}/changelog/latest.json
https://raw.githubusercontent.com/loudoguno/loudoguno-hub/main/{app-slug}/changelog/index.json
https://raw.githubusercontent.com/loudoguno/loudoguno-hub/main/{app-slug}/changelog/entries/v{X}.{Y}.{Z}.json
```

### Example: Fictionary

```bash
# Latest version
curl https://raw.githubusercontent.com/loudoguno/loudoguno-hub/main/fictionary/changelog/latest.json

# Full changelog
curl https://raw.githubusercontent.com/loudoguno/loudoguno-hub/main/fictionary/changelog/index.json

# Specific version
curl https://raw.githubusercontent.com/loudoguno/loudoguno-hub/main/fictionary/changelog/entries/v0.1.0.json
```

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md) for guidelines on submitting feature requests and bug reports.
