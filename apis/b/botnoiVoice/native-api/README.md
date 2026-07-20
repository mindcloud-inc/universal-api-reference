# Botnoi Voice: Native API Reference

A consolidated summary of Botnoi Voice's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://voice.botnoi.ai/developer/api
- **OpenAPI specification:** https://api-voice.botnoi.ai/openapi/v1/openapi.json
- **API base URL:** `https://api-voice.botnoi.ai`

## Authentication

### API Key

Connect with a Botnoi Voice API key obtained after AWS Marketplace activation.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://voice.botnoi.ai/developer/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Audio V1](actions/generate-audio-v1.md) | `POST /openapi/v1/generate_audio` | [docs](https://api-voice.botnoi.ai/openapi/v1/openapi.json) |
| [Generate Audio V2](actions/generate-audio-v2.md) | `POST /openapi/v1/generate_audio_v2` | [docs](https://api-voice.botnoi.ai/openapi/v1/openapi.json) |
| [List Speakers](actions/list-speakers.md) | `GET /openapi/v1/get_speaker_data_v2` | [docs](https://voice.botnoi.ai/developer/api) |
| [List Speakers V1](actions/list-speakers-v1.md) | `GET /openapi/v1/get_speaker_data` | [docs](https://api-voice.botnoi.ai/openapi/v1/openapi.json) |
