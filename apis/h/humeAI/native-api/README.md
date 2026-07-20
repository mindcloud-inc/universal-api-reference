# Hume AI: Native API Reference

A consolidated summary of Hume AI's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://dev.hume.ai/
- **API base URL:** `https://api.hume.ai`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Hume-Api-Key: <apiKey>
```

[Official authentication documentation](https://dev.hume.ai/docs/introduction/api-key)

### API Key (Header Only)

Send the Hume API key through the explicit X-Hume-Api-Key header template without bearer fallback.

### Credentials

- **API Key:** `apiKey` · required · Hume organization API key.

Send these headers with each API request:

```http
X-Hume-Api-Key: <apiKey>
```

[Official authentication documentation](https://dev.hume.ai/docs/introduction/api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Convert Voice File](actions/convert-voice-file.md) | `POST /v0/tts/voice_conversion/file` | [docs](https://dev.hume.ai/reference/text-to-speech-tts/convert-voice-file) |
| [Convert Voice JSON](actions/convert-voice-json.md) | `POST /v0/tts/voice_conversion/json` | [docs](https://dev.hume.ai/reference/text-to-speech-tts/convert-voice-json) |
| [Create Config](actions/create-config.md) | `POST /v0/evi/configs` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/configs/create-config) |
| [Create Prompt](actions/create-prompt.md) | `POST /v0/evi/prompts` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/prompts/create-prompt) |
| [Create Tool](actions/create-tool.md) | `POST /v0/evi/tools` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/tools/create-tool) |
| [Create Voice](actions/create-voice.md) | `POST /v0/tts/voices` | [docs](https://dev.hume.ai/reference/voices/create) |
| [Delete Config](actions/delete-config.md) | `DELETE /v0/evi/configs/:id` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/configs/delete-config) |
| [Delete Prompt](actions/delete-prompt.md) | `DELETE /v0/evi/prompts/:id` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/prompts/delete-prompt) |
| [Delete Tool](actions/delete-tool.md) | `DELETE /v0/evi/tools/:id` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/tools/delete-tool) |
| [Delete Voice](actions/delete-voice.md) | `DELETE /v0/tts/voices` | [docs](https://dev.hume.ai/reference/voices/delete) |
| [Get Config](actions/get-config.md) | `GET /v0/evi/configs/:id` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/configs/get-config) |
| [Get Prompt](actions/get-prompt.md) | `GET /v0/evi/prompts/:id` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/prompts/get-prompt) |
| [Get Tool](actions/get-tool.md) | `GET /v0/evi/tools/:id` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/tools/get-tool) |
| [List Configs](actions/list-configs.md) | `GET /v0/evi/configs` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/configs/list-configs) |
| [List Prompts](actions/list-prompts.md) | `GET /v0/evi/prompts` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/prompts/list-prompts) |
| [List Tools](actions/list-tools.md) | `GET /v0/evi/tools` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/tools/list-tools) |
| [List Voices](actions/list-voices.md) | `GET /v0/tts/voices` | [docs](https://dev.hume.ai/reference/voices/list) |
| [Stream Speech File](actions/stream-speech-file.md) | `POST /v0/tts/stream/file` | [docs](https://dev.hume.ai/reference/text-to-speech-tts/synthesize-file-streaming) |
| [Stream Speech JSON](actions/stream-speech-json.md) | `POST /v0/tts/stream/json` | [docs](https://dev.hume.ai/reference/text-to-speech-tts/synthesize-json-streaming) |
| [Synthesize Speech File](actions/synthesize-speech-file.md) | `POST /v0/tts/file` | [docs](https://dev.hume.ai/reference/text-to-speech-tts/synthesize-file) |
| [Synthesize Speech JSON](actions/synthesize-speech-json.md) | `POST /v0/tts` | [docs](https://dev.hume.ai/reference/text-to-speech-tts/synthesize-json) |
| [Update Config](actions/update-config.md) | `PATCH /v0/evi/configs/:id` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/configs/update-config) |
| [Update Prompt](actions/update-prompt.md) | `PATCH /v0/evi/prompts/:id` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/prompts/update-prompt) |
| [Update Tool](actions/update-tool.md) | `PATCH /v0/evi/tools/:id` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/tools/update-tool) |
