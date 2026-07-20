# Easy-Peasy.AI: Native API Reference

A consolidated summary of Easy-Peasy.AI's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://docs.easy-peasy.ai
- **OpenAPI specification:** https://docs.easy-peasy.ai/api-reference/openapi.json
- **REST API base URL:** `https://easy-peasy.ai`
- **Bots REST base URL:** `https://bots.easy-peasy.ai`

## Authentication

### API Key

Use an Easy-Peasy.AI API key from the settings page. The platform stores the secret as the implicit API key credential and sends it in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.easy-peasy.ai/api-reference/introduction)

## API conventions

### REST API

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

### Bots REST

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Chat Completions](actions/chat-completions.md) | `POST /api/chat/completions` | [docs](https://docs.easy-peasy.ai/api-reference/endpoint/chat-completions) |
| [Generate Sound Effect](actions/generate-sound-effect.md) | `POST /api/generate-sound` | [docs](https://docs.easy-peasy.ai/api-reference/endpoint/generate-sound) |
| [Generate Talking Video](actions/generate-talking-video.md) | `POST /api/generate-talking-video` | [docs](https://docs.easy-peasy.ai/api-reference/endpoint/generate-talking-video) |
| [Generate Text](actions/generate-text.md) | `POST /api/generate` | [docs](https://docs.easy-peasy.ai/api-reference/endpoint/generate) |
| [Generate Text-to-Speech](actions/generate-text-to-speech.md) | `POST /api/generate-text-to-speech` | [docs](https://docs.easy-peasy.ai/api-reference/endpoint/generate-tts) |
| [Get TTS Configuration](actions/get-tts-configuration.md) | `GET /api/get-text-to-speech-config` | [docs](https://docs.easy-peasy.ai/api-reference/endpoint/get-tts-config) |
| [Get TTS Voices](actions/get-tts-voices.md) | `GET /api/get-text-to-speech-voices` | [docs](https://docs.easy-peasy.ai/api-reference/endpoint/get-tts-voices) |
| [List Presets](actions/list-presets.md) | `GET /api/presets` | [docs](https://docs.easy-peasy.ai/api-reference/endpoint/list-presets) |
