# CAMB.AI: Native API Reference

A consolidated summary of CAMB.AI's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.camb.ai/api-reference
- **API base URL:** `https://client.camb.ai/apis`

## Authentication

### API Key

Authenticate with a CAMB.AI API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.camb.ai/getting-started/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Audio Separation](actions/create-audio-separation.md) | `POST /audio-separation` | [docs](https://docs.camb.ai/api-reference/endpoint/create-audio-separation) |
| [Create Custom Voice](actions/create-custom-voice.md) | `POST /create-custom-voice` | [docs](https://docs.camb.ai/api-reference/endpoint/create-custom-voice) |
| [Create Sound and Music](actions/create-sound-and-music.md) | `POST /text-to-sound` | [docs](https://docs.camb.ai/api-reference/endpoint/create-text-to-sound) |
| [Create Text-to-Speech](actions/create-text-to-speech.md) | `POST /tts` | [docs](https://docs.camb.ai/api-reference/endpoint/create-tts) |
| [Create Translated Text-to-Speech](actions/create-translated-text-to-speech.md) | `POST /translated-tts` | [docs](https://docs.camb.ai/api-reference/endpoint/create-translated-tts) |
| [Create Translation](actions/create-translation.md) | `POST /translate` | [docs](https://docs.camb.ai/api-reference/endpoint/create-translation) |
| [Create Voice from Description](actions/create-voice-from-description.md) | `POST /text-to-voice` | [docs](https://docs.camb.ai/api-reference/endpoint/create-text-to-voice) |
| [Fetch Bulk Sound and Music Results](actions/fetch-bulk-sound-and-music-results.md) | `POST /text-to-sound-results` | [docs](https://docs.camb.ai/api-reference/endpoint/fetch-text-to-sound-runs-results) |
| [Fetch Bulk Text-to-Speech Results](actions/fetch-bulk-text-to-speech-results.md) | `POST /tts-results` | [docs](https://docs.camb.ai/api-reference/endpoint/fetch-tts-runs-results) |
| [Fetch Bulk Translation Results](actions/fetch-bulk-translation-results.md) | `POST /translation-results` | [docs](https://docs.camb.ai/api-reference/endpoint/fetch-translation-runs-results) |
| [Get Audio Separation Result](actions/get-audio-separation-result.md) | `GET /audio-separation-result/:run_id` | [docs](https://docs.camb.ai/api-reference/endpoint/get-audio-separation-run-info) |
| [Get Audio Separation Task Status](actions/get-audio-separation-task-status.md) | `GET /audio-separation/:task_id` | [docs](https://docs.camb.ai/api-reference/endpoint/get-audio-separation-status) |
| [Get Sound and Music Result](actions/get-sound-and-music-result.md) | `GET /text-to-sound-result/:run_id` | [docs](https://docs.camb.ai/api-reference/endpoint/get-text-to-sound-run-result) |
| [Get Sound and Music Task Status](actions/get-sound-and-music-task-status.md) | `GET /text-to-sound/:task_id` | [docs](https://docs.camb.ai/api-reference/endpoint/get-text-to-sound-status) |
| [Get Source Languages](actions/get-source-languages.md) | `GET /source-languages` | [docs](https://docs.camb.ai/api-reference/endpoint/get-source-languages) |
| [Get Target Languages](actions/get-target-languages.md) | `GET /target-languages` | [docs](https://docs.camb.ai/api-reference/endpoint/get-target-languages) |
| [Get Text-to-Speech Result](actions/get-text-to-speech-result.md) | `GET /tts-result/:run_id` | [docs](https://docs.camb.ai/api-reference/endpoint/get-tts-run-info) |
| [Get Text-to-Speech Task Status](actions/get-text-to-speech-task-status.md) | `GET /tts/:task_id` | [docs](https://docs.camb.ai/api-reference/endpoint/get-tts-result) |
| [Get Translated Text-to-Speech Status](actions/get-translated-text-to-speech-status.md) | `GET /translated-tts/:task_id` | [docs](https://docs.camb.ai/api-reference/endpoint/poll-translated-tts-result) |
| [Get Translation Result](actions/get-translation-result.md) | `GET /translation-result/:run_id` | [docs](https://docs.camb.ai/api-reference/endpoint/get-translation-run-result) |
| [Get Translation Task Status](actions/get-translation-task-status.md) | `GET /translate/:task_id` | [docs](https://docs.camb.ai/api-reference/endpoint/poll-translation-result) |
| [Get Voice from Description Result](actions/get-voice-from-description-result.md) | `GET /text-to-voice-result/:run_id` | [docs](https://docs.camb.ai/api-reference/endpoint/get-text-to-voice-run-result) |
| [Get Voice from Description Task Status](actions/get-voice-from-description-task-status.md) | `GET /text-to-voice/:task_id` | [docs](https://docs.camb.ai/api-reference/endpoint/get-text-to-voice-status) |
| [List Voices](actions/list-voices.md) | `GET /list-voices` | [docs](https://docs.camb.ai/api-reference/endpoint/list-voices) |
