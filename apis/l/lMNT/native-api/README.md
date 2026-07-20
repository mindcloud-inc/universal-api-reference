# LMNT: Native API Reference

A consolidated summary of LMNT's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://docs.lmnt.com
- **OpenAPI specification:** https://api.lmnt.com/spec
- **API base URL:** `https://api.lmnt.com`

## Authentication

### API Key

Use your LMNT API key to authenticate requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://api.lmnt.com/spec)

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Account Info](actions/account-info.md) | `GET /v1/account` | [docs](https://docs.lmnt.com/api-reference/account-info) |
| [Create Voice](actions/create-voice.md) | `POST /v1/ai/voice` | [docs](https://docs.lmnt.com/api-reference/voice/create-voice) |
| [Delete Voice](actions/delete-voice.md) | `DELETE /v1/ai/voice/:id` | [docs](https://docs.lmnt.com/api-reference/voice/delete-voice) |
| [Generate Speech (Bytes)](actions/generate-speech-bytes.md) | `POST /v1/ai/speech/bytes` | [docs](https://docs.lmnt.com/api-reference/speech/synthesize-speech-bytes) |
| [Generate Speech (Detailed)](actions/generate-speech-detailed.md) | `POST /v1/ai/speech` | [docs](https://docs.lmnt.com/api-reference/speech/synthesize-speech-post) |
| [List Voices](actions/list-voices.md) | `GET /v1/ai/voice/list` | [docs](https://docs.lmnt.com/api-reference/voice/list-voices) |
| [Update Voice](actions/update-voice.md) | `PUT /v1/ai/voice/:id` | [docs](https://docs.lmnt.com/api-reference/voice/update-voice) |
| [Voice Info](actions/voice-info.md) | `GET /v1/ai/voice/:id` | [docs](https://docs.lmnt.com/api-reference/voice/voice-info) |
