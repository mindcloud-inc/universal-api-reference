# Uberduck: Native API Reference

A consolidated summary of Uberduck's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://docs.uberduck.ai/api-reference/introduction
- **API base URL:** `https://api.uberduck.ai`

## Authentication

### API Key

Authenticate with an Uberduck API key sent as Authorization: Bearer <api_key>.

### Credentials

- **API Key:** `apiKey` · required · Your Uberduck API key.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.uberduck.ai/api-reference/authentication)

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Models](actions/get-models.md) | `GET /v1/models` | [docs](https://docs.uberduck.ai/api-reference/get-models-v-1-models-get) |
| [Instant Voice Clone](actions/instant-voice-clone.md) | `POST /v1/voices` | [docs](https://docs.uberduck.ai/api-reference/instant-voice-clone-v-1-voices-post) |
| [List Voices](actions/list-voices.md) | `GET /v1/voices` | [docs](https://docs.uberduck.ai/api-reference/get-voices-v-1-voices-get) |
| [Text To Speech](actions/text-to-speech.md) | `POST /v1/text-to-speech` | [docs](https://docs.uberduck.ai/api-reference/text-to-speech-v-1-text-to-speech-post) |
