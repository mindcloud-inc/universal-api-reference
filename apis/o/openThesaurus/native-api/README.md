# OpenThesaurus: Native API Reference

A consolidated summary of OpenThesaurus's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://www.openthesaurus.de/about/api
- **API base URL:** `https://www.openthesaurus.de/synonyme/search`

## Authentication

### Public API

No authentication required for the OpenThesaurus public search API.

This API does not require request authentication.

[Official authentication documentation](https://www.openthesaurus.de/about/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |
| `User-Agent` | `MindCloud Codex https://mindcloud.co` |

Responses from this API use JSON.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Search Synonyms](actions/search-synonyms.md) | `GET /` | [docs](https://www.openthesaurus.de/about/api) |
