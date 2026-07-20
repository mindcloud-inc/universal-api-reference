# Free Dictionary: Native API Reference

A consolidated summary of Free Dictionary's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://dictionaryapi.dev/
- **API base URL:** `https://api.dictionaryapi.dev`

## Authentication

### No Auth

The Free Dictionary API is public and does not require authentication.

This API does not require request authentication.

[Official authentication documentation](https://dictionaryapi.dev/)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Word Entries](actions/get-word-entries.md) | `GET /api/v2/entries/:language/:word` | [docs](https://dictionaryapi.dev/) |
| [Get Word Entries (Legacy v1)](actions/get-word-entries-legacy-v1.md) | `GET /api/v1/entries/:language/:word` | [docs](https://github.com/meetDeveloper/freeDictionaryAPI#regarding-v1-version) |
