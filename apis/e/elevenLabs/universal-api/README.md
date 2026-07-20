# <img src="https://images.mindcloud.co/apps/icons/eleven-labs_1773238483397.png" alt="ElevenLabs logo" width="28" height="28"> ElevenLabs: Universal API

Create voices, generate speech, dub media, and transcribe audio

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/elevenLabs/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://elevenlabs.io
- **Vendor API docs:** https://elevenlabs.io/docs/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/elevenLabs/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Dialogue Audio

| Action | Method | Description |
| --- | --- | --- |
| [Create Dialogue](actions/create-dialogue.md) | POST | Creates dialogue audio from text in ElevenLabs. |

### Dialogue Audio Stream

| Action | Method | Description |
| --- | --- | --- |
| [Stream Dialogue](actions/stream-dialogue.md) | POST | Streams dialogue audio from text in ElevenLabs. |

### Forced Alignment

| Action | Method | Description |
| --- | --- | --- |
| [Create Forced Alignment](actions/create-forced-alignment.md) | POST | Creates forced alignment data from audio in ElevenLabs. |

### History Item

| Action | Method | Description |
| --- | --- | --- |
| [Get History Item](actions/get-history-item.md) | GET | Retrieves a generated audio item from ElevenLabs. |
| [List Generated Items](actions/list-generated-items.md) | GET | Retrieves previously generated audio from ElevenLabs. |

### Isolated Audio

| Action | Method | Description |
| --- | --- | --- |
| [Isolate Audio](actions/isolate-audio.md) | POST | Removes background noise from audio in ElevenLabs. |

### Isolated Audio Stream

| Action | Method | Description |
| --- | --- | --- |
| [Stream Audio Isolation](actions/stream-audio-isolation.md) | POST | Streams audio with background noise removed from ElevenLabs. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [List Models](actions/list-models.md) | GET | Retrieves a list of models from ElevenLabs. |

### Single Use Token

| Action | Method | Description |
| --- | --- | --- |
| [Create Single Use Token](actions/create-single-use-token.md) | POST | Creates a single-use token in ElevenLabs. |

### Sound Effect

| Action | Method | Description |
| --- | --- | --- |
| [Create Sound Effect](actions/create-sound-effect.md) | POST | Creates sound effect audio from text in ElevenLabs. |

### Speech Audio

| Action | Method | Description |
| --- | --- | --- |
| [Convert Speech To Speech](actions/convert-speech-to-speech.md) | POST | Transforms audio from one voice to another in ElevenLabs. |
| [Create Speech](actions/create-speech.md) | POST | Creates speech audio from text in ElevenLabs. |

### Speech Audio Stream

| Action | Method | Description |
| --- | --- | --- |
| [Stream Speech](actions/stream-speech.md) | POST | Streams speech audio from text in ElevenLabs. |
| [Stream Speech To Speech](actions/stream-speech-to-speech.md) | POST | Streams audio transformed between voices in ElevenLabs. |

### Speech Timing

| Action | Method | Description |
| --- | --- | --- |
| [Create Speech with Timing](actions/create-speech-with-timing.md) | POST | Creates speech audio with timestamps in ElevenLabs. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Get User Subscription](actions/get-user-subscription.md) | GET | Retrieves a user subscription from ElevenLabs. |

### Transcript

| Action | Method | Description |
| --- | --- | --- |
| [Create Transcript](actions/create-transcript.md) | POST | Creates a transcript from audio or video in ElevenLabs. |
| [Delete Transcript](actions/delete-transcript.md) | DELETE | Deletes an existing transcript from ElevenLabs. |
| [Get Transcript](actions/get-transcript.md) | GET | Retrieves a transcript from ElevenLabs. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from ElevenLabs. |

### Voice

| Action | Method | Description |
| --- | --- | --- |
| [Get Voice](actions/get-voice.md) | GET | Retrieves a voice from ElevenLabs. |
| [List Voices](actions/list-voices.md) | GET | Retrieves a list of voices from ElevenLabs. |

### Voice Sample Audio

| Action | Method | Description |
| --- | --- | --- |
| [Get Voice Sample Audio](actions/get-voice-sample-audio.md) | GET | Retrieves voice sample audio from ElevenLabs. |

### Voice Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Voice Settings](actions/get-voice-settings.md) | GET | Retrieves voice settings from ElevenLabs. |

