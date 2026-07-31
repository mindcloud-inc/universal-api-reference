# Useless Facts: Native API Reference

A consolidated summary of Useless Facts's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://uselessfacts.jsph.pl/
- **API base URL:** `https://uselessfacts.jsph.pl`

## Authentication

### No Authentication

This API does not require request authentication.

[Official authentication documentation](https://uselessfacts.jsph.pl/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Fetch Random Useless Fact](actions/fetch-random-useless-fact.md) | `GET /api/v2/facts/random` | [docs](https://uselessfacts.jsph.pl/) |
| [Fetch Useless Fact of the Day](actions/fetch-useless-fact-of-the-day.md) | `GET /api/v2/facts/today` | [docs](https://uselessfacts.jsph.pl/) |
