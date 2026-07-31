# Fun Translations: Native API Reference

A consolidated summary of Fun Translations's API configuration and 6 documented operations.

- **API base URL:** `https://api.funtranslations.com/translate`

## Authentication

### API key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://funtranslations.com/api/yodish)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Translate to Dothraki](actions/translate-dothraki.md) | `POST /dothraki` | [docs](https://funtranslations.com/api/yodish) |
| [Translate to Klingon](actions/translate-klingon.md) | `POST /klingon` | [docs](https://funtranslations.com/api/yodish) |
| [Translate to Minion](actions/translate-minion.md) | `POST /minion` | [docs](https://funtranslations.com/api/yodish) |
| [Translate to Pirate](actions/translate-pirate.md) | `POST /pirate` | [docs](https://funtranslations.com/api/yodish) |
| [Translate to Shakespeare](actions/translate-shakespeare.md) | `POST /shakespeare` | [docs](https://funtranslations.com/api/yodish) |
| [Translate to Yoda](actions/translate-yoda.md) | `POST /yodish` | [docs](https://funtranslations.com/api/yodish) |
