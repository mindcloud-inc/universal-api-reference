# Voicemaker: Native API Reference

A consolidated summary of Voicemaker's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://developer.voicemaker.in/apidocs/introduction
- **API base URL:** `https://developer.voicemaker.in`

## Authentication

### API Key

Use a Voicemaker API key. Requests are authenticated with Authorization: Bearer <API key>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.voicemaker.in/apidocs/authentication)

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Convert Speech to Speech](actions/convert-speech-to-speech.md) | `POST api/v1/speech-to-speech` | [docs](https://developer.voicemaker.in/apidocs/speech-to-speech-api) |
| [Create Transcription](actions/create-transcription.md) | `POST api/v1/speech-to-text` | [docs](https://developer.voicemaker.in/apidocs/speech-to-text-api) |
| [Create Voice Clone](actions/create-voice-clone.md) | `POST api/v1/voice-clones/add` | [docs](https://developer.voicemaker.in/apidocs/create-voice-clone) |
| [Delete Voice Clone](actions/delete-voice-clone.md) | `DELETE api/v1/voice-clones/{VoiceId}` | [docs](https://developer.voicemaker.in/apidocs/delete-voice-clone) |
| [Generate TTS](actions/generate-tts.md) | `POST api/v1/voice/convert` | [docs](https://developer.voicemaker.in/apidocs/generate-tts) |
| [Generate TTS with VoxFX](actions/generate-tts-with-vox-fx.md) | `POST api/v1/voice/convert` | [docs](https://developer.voicemaker.in/apidocs/generate-tts-with-voxfx) |
| [Get Transcription](actions/get-transcription.md) | `GET api/v1/speech-to-text/{taskId}` | [docs](https://developer.voicemaker.in/apidocs/get-single-transcription-api) |
| [Get Voice Clone](actions/get-voice-clone.md) | `GET api/v1/voice-clones/{VoiceId}` | [docs](https://developer.voicemaker.in/apidocs/get-single-voice) |
| [List Transcription Files](actions/list-transcription-files.md) | `GET api/v1/speech-to-text` | [docs](https://developer.voicemaker.in/apidocs/list-transcription-files-api) |
| [List Voice Clones](actions/list-voice-clones.md) | `GET api/v1/voice-clones` | [docs](https://developer.voicemaker.in/apidocs/list-all-voice-clones) |
| [List Voices](actions/list-voices.md) | `POST api/v1/voice/list` | [docs](https://developer.voicemaker.in/apidocs/list-of-all-voices) |
| [List VoxFX Effects](actions/list-vox-fx-effects.md) | `GET effects/voxfx` | [docs](https://developer.voicemaker.in/apidocs/list-of-all-voxfx) |
| [Update Voice Clone](actions/update-voice-clone.md) | `PUT api/v1/voice-clones/{VoiceId}` | [docs](https://developer.voicemaker.in/apidocs/edit-voice-clone) |
