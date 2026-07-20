# Murf Core: Native API Reference

A consolidated summary of Murf Core's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://murf.ai/api/docs/introduction/overview
- **API base URL:** `https://api.murf.ai`

## Authentication

### API Key

Connect to Murf Core with a Murf API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
api-key: <apiKey>
```

[Official authentication documentation](https://murf.ai/api/docs/introduction/quickstart)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Voices](actions/list-voices.md) | `GET /v1/speech/voices` | [docs](https://murf.ai/api/docs/api-reference/voices/get-voices) |
| [Synthesize Speech](actions/synthesize-speech.md) | `POST /v1/speech/generate` | [docs](https://murf.ai/api/docs/api-reference/text-to-speech/generate) |
| [Translate Text](actions/translate-text.md) | `POST /v1/text/translate` | [docs](https://murf.ai/api/docs/api-reference/translation/translate) |
| [Voice Changer](actions/voice-changer.md) | `POST /v1/voice-changer/convert` | [docs](https://murf.ai/api/docs/api-reference/voice-changer/convert) |
