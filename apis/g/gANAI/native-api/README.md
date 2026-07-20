# GAN.AI: Native API Reference

A consolidated summary of GAN.AI's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://developer.gan.ai/api-reference
- **OpenAPI specification:** https://developer.gan.ai/openapi.json
- **API base URL:** `https://os.gan.ai`

## Authentication

### API Key

Use a GAN.AI API key in the ganos-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
ganos-api-key: <apiKey>
```

[Official authentication documentation](https://developer.gan.ai/api-reference/voices/get-voices)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size. Use `skip` in the query string as the record offset.

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Voice](actions/add-voice.md) | `POST /v1/voices` | [docs](https://developer.gan.ai/api-reference/voices/add-voice) |
| [Create Avatar](actions/create-avatar.md) | `POST /v1/avatars/create_avatar` | [docs](https://developer.gan.ai/api-reference/avatars/create-avatar) |
| [Create Avatar Video](actions/create-avatar-video.md) | `POST /v1/avatars/create_video` | [docs](https://developer.gan.ai/api-reference/avatars/create-video) |
| [Create LipSync](actions/create-lip-sync.md) | `POST /v1/lipsync/create_lipsync` | [docs](https://developer.gan.ai/api-reference/lipsync/create-lipsync) |
| [Create Photo Avatar](actions/create-photo-avatar.md) | `POST /v1/photo_avatars/create` | [docs](https://developer.gan.ai/api-reference/photo-avatars/create) |
| [Create Photo Avatar Inference](actions/create-photo-avatar-inference.md) | `POST /v1/photo_avatars/create_inference` | [docs](https://developer.gan.ai/api-reference/photo-avatars/create-inference) |
| [Delete Avatar Videos Bulk](actions/delete-avatar-videos-bulk.md) | `DELETE /v1/avatars/bulk_delete_avatar_inferences` | [docs](https://developer.gan.ai/api-reference/avatars/bulk-delete-avatar-inferences) |
| [Delete Avatars](actions/delete-avatars.md) | `DELETE /v1/avatars/bulk_delete_avatars` | [docs](https://developer.gan.ai/api-reference/avatars/bulk-delete-avatars) |
| [Delete LipSync Videos Bulk](actions/delete-lip-sync-videos-bulk.md) | `DELETE /v1/lipsync/bulk_delete_lipsyncs` | [docs](https://developer.gan.ai/api-reference/lipsync/bulk-delete-lipsyncs) |
| [Delete Voice](actions/delete-voice.md) | `DELETE /v1/voices/[:voice_id]` | [docs](https://developer.gan.ai/api-reference/voices/delete-voice) |
| [Generate Sound Effect](actions/generate-sound-effect.md) | `POST /v1/sfx/generate` | [docs](https://developer.gan.ai/api-reference/sound-effects/generate) |
| [Generate Speech](actions/generate-speech.md) | `POST /v1/tts` | [docs](https://developer.gan.ai/api-reference/text-to-speech/tts-sync-api) |
| [Get Avatar Details](actions/get-avatar-details.md) | `GET /v1/avatars/avatar_details` | [docs](https://developer.gan.ai/api-reference/avatars/avatar-details) |
| [Get Avatar Video Details](actions/get-avatar-video-details.md) | `GET /v1/avatars/inference_details` | [docs](https://developer.gan.ai/api-reference/avatars/get-avatar-inference-details) |
| [Get Consent Passcode](actions/get-consent-passcode.md) | `GET /v1/consents/consent_passcode` | [docs](https://developer.gan.ai/api-reference/consent/get-consent-passcode) |
| [Get LipSync Inference Details](actions/get-lip-sync-inference-details.md) | `GET /v1/lipsync/inference_details` | [docs](https://developer.gan.ai/api-reference/lipsync/inference-details) |
| [Get Photo Avatar Details](actions/get-photo-avatar-details.md) | `GET /v1/photo_avatars/details` | [docs](https://developer.gan.ai/api-reference/photo-avatars/details) |
| [Get Photo Avatar Inference Details](actions/get-photo-avatar-inference-details.md) | `GET /v1/photo_avatars/inference_details` | [docs](https://developer.gan.ai/api-reference/photo-avatars/inference-details) |
| [Get Sound Effect Audio](actions/get-sound-effect-audio.md) | `POST /v1/sfx/audio` | [docs](https://developer.gan.ai/api-reference/sound-effects/audio) |
| [List Avatar Videos](actions/list-avatar-videos.md) | `GET /v1/avatars/list_inferences` | [docs](https://developer.gan.ai/api-reference/avatars/avatar-inferences-list) |
| [List Avatars](actions/list-avatars.md) | `GET /v1/avatars/list` | [docs](https://developer.gan.ai/api-reference/avatars/get-avatar-list-for-user) |
| [List Photo Avatar Inferences](actions/list-photo-avatar-inferences.md) | `GET /v1/photo_avatars/list_inference` | [docs](https://developer.gan.ai/api-reference/photo-avatars/list-inference) |
| [List Photo Avatars](actions/list-photo-avatars.md) | `GET /v1/photo_avatars/list` | [docs](https://developer.gan.ai/api-reference/photo-avatars/list) |
| [List Sound Effect History](actions/list-sound-effect-history.md) | `GET /v1/sfx/history` | [docs](https://developer.gan.ai/api-reference/sound-effects/history) |
| [List Text to Speech History](actions/list-text-to-speech-history.md) | `GET /v1/tts/history` | [docs](https://developer.gan.ai/api-reference/text-to-speech/tts-history) |
| [List User LipSyncs](actions/list-user-lip-syncs.md) | `GET /v1/lipsync/get_user_lipsyncs` | [docs](https://developer.gan.ai/api-reference/lipsync/get-user-lipsyncs) |
| [List Voices](actions/list-voices.md) | `GET /v1/voices` | [docs](https://developer.gan.ai/api-reference/voices/get-voices) |
| [Submit Consent](actions/submit-consent.md) | `POST /v1/consents/submit_consent` | [docs](https://developer.gan.ai/api-reference/consent/submit-consent) |
