# Runway: Native API Reference

A consolidated summary of Runway's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://docs.dev.runwayml.com/api/
- **API base URL:** `https://api.dev.runwayml.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.dev.runwayml.com/guides/setup/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100). Use `cursor` in the query string as the pagination cursor.

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Or Delete Task](actions/cancel-or-delete-task.md) | `DELETE /v1/tasks/[:id]` | [docs](https://docs.dev.runwayml.com/api#tag/Task-management/paths/~1v1~1tasks~1%7Bid%7D/delete) |
| [Cancel Realtime Session](actions/cancel-realtime-session.md) | `DELETE /v1/realtime_sessions/[:id]` | [docs](https://docs.dev.runwayml.com/api#tag/Realtime-Sessions/paths/~1v1~1realtime_sessions~1%7Bid%7D/delete) |
| [Control A Character](actions/control-a-character.md) | `POST /v1/character_performance` | [docs](https://docs.dev.runwayml.com/api#tag/Start-generating/paths/~1v1~1character_performance/post) |
| [Create Avatar](actions/create-avatar.md) | `POST /v1/avatars` | [docs](https://docs.dev.runwayml.com/api#tag/Avatars/paths/~1v1~1avatars/post) |
| [Create Document](actions/create-document.md) | `POST /v1/documents` | [docs](https://docs.dev.runwayml.com/api#tag/Knowledge/paths/~1v1~1documents/post) |
| [Create Realtime Session](actions/create-realtime-session.md) | `POST /v1/realtime_sessions` | [docs](https://docs.dev.runwayml.com/api#tag/Realtime-Sessions/paths/~1v1~1realtime_sessions/post) |
| [Delete Avatar](actions/delete-avatar.md) | `DELETE /v1/avatars/[:id]` | [docs](https://docs.dev.runwayml.com/api#tag/Avatars/paths/~1v1~1avatars~1%7Bid%7D/delete) |
| [Delete Document](actions/delete-document.md) | `DELETE /v1/documents/[:id]` | [docs](https://docs.dev.runwayml.com/api#tag/Knowledge/paths/~1v1~1documents~1%7Bid%7D/delete) |
| [Delete Voice](actions/delete-voice.md) | `DELETE /v1/voices/[:id]` | [docs](https://docs.dev.runwayml.com/api#tag/Voices/paths/~1v1~1voices~1%7Bid%7D/delete) |
| [Generate Sound Effects](actions/generate-sound-effects.md) | `POST /v1/sound_effect` | [docs](https://docs.dev.runwayml.com/api#tag/Start-generating/paths/~1v1~1sound_effect/post) |
| [Get Avatar](actions/get-avatar.md) | `GET /v1/avatars/[:id]` | [docs](https://docs.dev.runwayml.com/api#tag/Avatars/paths/~1v1~1avatars~1%7Bid%7D/get) |
| [Get Document](actions/get-document.md) | `GET /v1/documents/[:id]` | [docs](https://docs.dev.runwayml.com/api#tag/Knowledge/paths/~1v1~1documents~1%7Bid%7D/get) |
| [Get Organization Information](actions/get-organization-information.md) | `GET /v1/organization` | [docs](https://docs.dev.runwayml.com/api#tag/Organization/paths/~1v1~1organization/get) |
| [Get Realtime Session](actions/get-realtime-session.md) | `GET /v1/realtime_sessions/[:id]` | [docs](https://docs.dev.runwayml.com/api#tag/Realtime-Sessions/paths/~1v1~1realtime_sessions~1%7Bid%7D/get) |
| [Get Task Detail](actions/get-task-detail.md) | `GET /v1/tasks/[:id]` | [docs](https://docs.dev.runwayml.com/api#tag/Task-management/paths/~1v1~1tasks~1%7Bid%7D/get) |
| [Get Voice](actions/get-voice.md) | `GET /v1/voices/[:id]` | [docs](https://docs.dev.runwayml.com/api#tag/Voices/paths/~1v1~1voices~1%7Bid%7D/get) |
| [Image To Video](actions/image-to-video.md) | `POST /v1/image_to_video` | [docs](https://docs.dev.runwayml.com/api#tag/Start-generating/paths/~1v1~1image_to_video/post) |
| [List Avatars](actions/list-avatars.md) | `GET /v1/avatars` | [docs](https://docs.dev.runwayml.com/api#tag/Avatars/paths/~1v1~1avatars/get) |
| [List Documents](actions/list-documents.md) | `GET /v1/documents` | [docs](https://docs.dev.runwayml.com/api#tag/Knowledge/paths/~1v1~1documents/get) |
| [List Voices](actions/list-voices.md) | `GET /v1/voices` | [docs](https://docs.dev.runwayml.com/api#tag/Voices/paths/~1v1~1voices/get) |
| [Preview Voice](actions/preview-voice.md) | `POST /v1/voices/preview` | [docs](https://docs.dev.runwayml.com/api#tag/Voices/paths/~1v1~1voices~1preview/post) |
| [Query Credit Usage](actions/query-credit-usage.md) | `POST /v1/organization/usage` | [docs](https://docs.dev.runwayml.com/api#tag/Organization/paths/~1v1~1organization~1usage/post) |
| [Speech To Speech](actions/speech-to-speech.md) | `POST /v1/speech_to_speech` | [docs](https://docs.dev.runwayml.com/api#tag/Start-generating/paths/~1v1~1speech_to_speech/post) |
| [Text Or Image To Image](actions/text-or-image-to-image.md) | `POST /v1/text_to_image` | [docs](https://docs.dev.runwayml.com/api#tag/Start-generating/paths/~1v1~1text_to_image/post) |
| [Text To Speech](actions/text-to-speech.md) | `POST /v1/text_to_speech` | [docs](https://docs.dev.runwayml.com/api#tag/Start-generating/paths/~1v1~1text_to_speech/post) |
| [Text To Video](actions/text-to-video.md) | `POST /v1/text_to_video` | [docs](https://docs.dev.runwayml.com/api#tag/Start-generating/paths/~1v1~1text_to_video/post) |
| [Update Avatar](actions/update-avatar.md) | `PATCH /v1/avatars/[:id]` | [docs](https://docs.dev.runwayml.com/api#tag/Avatars/paths/~1v1~1avatars~1%7Bid%7D/patch) |
| [Update Document](actions/update-document.md) | `PATCH /v1/documents/[:id]` | [docs](https://docs.dev.runwayml.com/api#tag/Knowledge/paths/~1v1~1documents~1%7Bid%7D/patch) |
| [Upload File](actions/upload-file.md) | `POST /v1/uploads` | [docs](https://docs.dev.runwayml.com/api#tag/Uploads/paths/~1v1~1uploads/post) |
| [Video To Video](actions/video-to-video.md) | `POST /v1/video_to_video` | [docs](https://docs.dev.runwayml.com/api#tag/Start-generating/paths/~1v1~1video_to_video/post) |
| [Voice Dubbing](actions/voice-dubbing.md) | `POST /v1/voice_dubbing` | [docs](https://docs.dev.runwayml.com/api#tag/Start-generating/paths/~1v1~1voice_dubbing/post) |
| [Voice Isolation](actions/voice-isolation.md) | `POST /v1/voice_isolation` | [docs](https://docs.dev.runwayml.com/api#tag/Start-generating/paths/~1v1~1voice_isolation/post) |
