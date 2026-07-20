# TypeCast: Native API Reference

A consolidated summary of TypeCast's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://typecast.ai/docs/api-reference
- **OpenAPI specification:** https://typecast.ai/docs/api-reference/openapi.json
- **API base URL:** `https://api.typecast.ai/`

## Authentication

### API Key

Connect with your TypeCast API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://typecast.ai/docs/quickstart)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Subscription](actions/get-subscription.md) | `GET /v1/users/me/subscription` | [docs](https://typecast.ai/docs/api-reference/subscription/get-subscription) |
| [Get Voice Details](actions/get-voice-details.md) | `GET /v2/voices/:voice_id` | [docs](https://typecast.ai/docs/api-reference/voices/get-voice-details) |
| [List Voices](actions/list-voices.md) | `GET /v2/voices` | [docs](https://typecast.ai/docs/api-reference/voices/list-voices) |
| [Streaming Text To Speech](actions/streaming-text-to-speech.md) | `POST /v1/text-to-speech/stream` | [docs](https://typecast.ai/docs/api-reference/text-to-speech/streaming-text-to-speech) |
| [Text To Speech](actions/text-to-speech.md) | `POST /v1/text-to-speech` | [docs](https://typecast.ai/docs/api-reference/text-to-speech/text-to-speech) |
