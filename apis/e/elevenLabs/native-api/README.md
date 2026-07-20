# ElevenLabs: Native API Reference

A consolidated summary of ElevenLabs's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://elevenlabs.io/docs/api-reference/introduction
- **API base URL:** `https://api.elevenlabs.io/v1`

## Authentication

### Custom API Key

Connect with an ElevenLabs API key sent as the xi-api-key header.

### Credentials

- **API Key:** `apiKey` · required · Your ElevenLabs API key.

Send these headers with each API request:

```http
xi-api-key: <apiKey>
```

[Official authentication documentation](https://elevenlabs.io/docs/api-reference/authentication)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Convert Speech To Speech](actions/convert-speech-to-speech.md) | `POST /speech-to-speech/:voice_id` | [docs](https://elevenlabs.io/docs/api-reference/speech-to-speech/convert) |
| [Create Dialogue](actions/create-dialogue.md) | `POST /text-to-dialogue` | [docs](https://elevenlabs.io/docs/api-reference/text-to-dialogue/convert) |
| [Create Forced Alignment](actions/create-forced-alignment.md) | `POST /forced-alignment` | [docs](https://elevenlabs.io/docs/api-reference/forced-alignment/create) |
| [Create Single Use Token](actions/create-single-use-token.md) | `POST /single-use-token/:token_type` | [docs](https://elevenlabs.io/docs/api-reference/tokens/create) |
| [Create Sound Effect](actions/create-sound-effect.md) | `POST /sound-generation` | [docs](https://elevenlabs.io/docs/api-reference/text-to-sound-effects/convert) |
| [Create Speech](actions/create-speech.md) | `POST /text-to-speech/:voice_id` | [docs](https://elevenlabs.io/docs/api-reference/text-to-speech/convert) |
| [Create Speech with Timing](actions/create-speech-with-timing.md) | `POST /text-to-speech/:voice_id/with-timestamps` | [docs](https://elevenlabs.io/docs/api-reference/text-to-speech/convert-with-timestamps) |
| [Create Transcript](actions/create-transcript.md) | `POST /speech-to-text` | [docs](https://elevenlabs.io/docs/api-reference/speech-to-text/convert) |
| [Delete Transcript](actions/delete-transcript.md) | `DELETE /speech-to-text/transcripts/:transcription_id` | [docs](https://elevenlabs.io/docs/api-reference/speech-to-text/delete) |
| [Get History Item](actions/get-history-item.md) | `GET /history/:history_item_id` | [docs](https://elevenlabs.io/docs/api-reference/history/get) |
| [Get Transcript](actions/get-transcript.md) | `GET /speech-to-text/transcripts/:transcription_id` | [docs](https://elevenlabs.io/docs/api-reference/speech-to-text/get) |
| [Get User](actions/get-user.md) | `GET /user` | [docs](https://elevenlabs.io/docs/api-reference/user/get) |
| [Get User Subscription](actions/get-user-subscription.md) | `GET /user/subscription` | [docs](https://elevenlabs.io/docs/api-reference/user/subscription/get) |
| [Get Voice](actions/get-voice.md) | `GET /voices/:voice_id` | [docs](https://elevenlabs.io/docs/api-reference/voices/get) |
| [Get Voice Sample Audio](actions/get-voice-sample-audio.md) | `GET /voices/:voice_id/samples/:sample_id/audio` | [docs](https://elevenlabs.io/docs/api-reference/voices/samples/get) |
| [Get Voice Settings](actions/get-voice-settings.md) | `GET /voices/:voice_id/settings` | [docs](https://elevenlabs.io/docs/api-reference/voices/settings/get) |
| [Isolate Audio](actions/isolate-audio.md) | `POST /audio-isolation` | [docs](https://elevenlabs.io/docs/api-reference/audio-isolation/convert) |
| [List Generated Items](actions/list-generated-items.md) | `GET /history` | [docs](https://elevenlabs.io/docs/api-reference/history/list) |
| [List Models](actions/list-models.md) | `GET /models` | [docs](https://elevenlabs.io/docs/api-reference/models/list) |
| [List Voices](actions/list-voices.md) | `GET /voices` | [docs](https://elevenlabs.io/docs/api-reference/voices/search) |
| [Stream Audio Isolation](actions/stream-audio-isolation.md) | `POST /audio-isolation/stream` | [docs](https://elevenlabs.io/docs/api-reference/audio-isolation/stream) |
| [Stream Dialogue](actions/stream-dialogue.md) | `POST /text-to-dialogue/stream` | [docs](https://elevenlabs.io/docs/api-reference/text-to-dialogue/stream) |
| [Stream Speech](actions/stream-speech.md) | `POST /text-to-speech/:voice_id/stream` | [docs](https://elevenlabs.io/docs/api-reference/text-to-speech/stream) |
| [Stream Speech To Speech](actions/stream-speech-to-speech.md) | `POST /speech-to-speech/:voice_id/stream` | [docs](https://elevenlabs.io/docs/api-reference/speech-to-speech/stream) |
