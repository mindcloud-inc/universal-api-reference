# <img src="https://images.mindcloud.co/apps/icons/voicemaker-icon_1776352476133.png" alt="Voicemaker logo" width="28" height="28"> Voicemaker: Universal API

Voicemaker provides text-to-speech, VoxFX voice effects, voice cloning, speech-to-speech conversion, and speech-to-text APIs for generating and transforming audio.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/voicemaker/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://voicemaker.in
- **Vendor API docs:** https://developer.voicemaker.in/apidocs/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List VoxFX Effects](actions/list-vox-fx-effects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/list-vox-fx-effects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Create Transcription](actions/create-transcription.md) | POST | Creates a transcription from audio in Voicemaker. |
| [Get Transcription](actions/get-transcription.md) | GET | Retrieves a single transcription from Voicemaker. |
| [List Transcription Files](actions/list-transcription-files.md) | GET | Retrieves all transcription files from Voicemaker. |

### Models

| Action | Method | Description |
| --- | --- | --- |
| [Create Voice Clone](actions/create-voice-clone.md) | POST | Creates a new voice clone in Voicemaker. |
| [Delete Voice Clone](actions/delete-voice-clone.md) | DELETE | Deletes an existing voice clone from Voicemaker. |
| [Get Voice Clone](actions/get-voice-clone.md) | GET | Retrieves a single voice clone from Voicemaker. |
| [List Voice Clones](actions/list-voice-clones.md) | GET | Retrieves all voice clones from Voicemaker. |
| [List Voices](actions/list-voices.md) | GET | Retrieves all available voices from Voicemaker. |
| [Update Voice Clone](actions/update-voice-clone.md) | PUT | Updates an existing voice clone in Voicemaker. |

### Recordings

| Action | Method | Description |
| --- | --- | --- |
| [Convert Speech to Speech](actions/convert-speech-to-speech.md) | POST | Creates converted speech from uploaded audio in Voicemaker. |
| [Generate TTS](actions/generate-tts.md) | POST | Creates synthesized speech from text in Voicemaker. |
| [Generate TTS with VoxFX](actions/generate-tts-with-vox-fx.md) | POST | Creates synthesized speech with VoxFX in Voicemaker. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [List VoxFX Effects](actions/list-vox-fx-effects.md) | GET | Retrieves available VoxFX effects from Voicemaker. |

