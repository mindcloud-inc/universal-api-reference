# <img src="https://images.mindcloud.co/apps/icons/camb-ai-w2jtco_1776968797660.png" alt="CAMB.AI logo" width="28" height="28"> CAMB.AI: Universal API

Generate speech, translations, dubbing, and audio content

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cAMBAI/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://camb.ai
- **Vendor API docs:** https://docs.camb.ai/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Voices](actions/list-voices.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/list-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Audio Separation Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Audio Separation Result](actions/get-audio-separation-result.md) | GET | Retrieves an audio separation result from CAMB.AI. |

### Audio Separation Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Audio Separation](actions/create-audio-separation.md) | POST | Creates a new audio separation task in CAMB.AI. |

### Audio Separation Task Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Audio Separation Task Status](actions/get-audio-separation-task-status.md) | GET | Retrieves audio separation task status from CAMB.AI. |

### Custom Voice

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Voice](actions/create-custom-voice.md) | POST | Creates a new custom voice in CAMB.AI. |

### Language

| Action | Method | Description |
| --- | --- | --- |
| [Get Source Languages](actions/get-source-languages.md) | GET | Retrieves supported source languages from CAMB.AI. |
| [Get Target Languages](actions/get-target-languages.md) | GET | Retrieves supported target languages from CAMB.AI. |

### Sound And Music Result

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Bulk Sound and Music Results](actions/fetch-bulk-sound-and-music-results.md) | GET | Retrieves multiple sound and music results from CAMB.AI. |
| [Get Sound and Music Result](actions/get-sound-and-music-result.md) | GET | Retrieves a sound or music result from CAMB.AI. |

### Sound And Music Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Sound and Music](actions/create-sound-and-music.md) | POST | Creates a new sound or music task in CAMB.AI. |

### Sound And Music Task Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Sound and Music Task Status](actions/get-sound-and-music-task-status.md) | GET | Retrieves sound and music task status from CAMB.AI. |

### Text-to-speech Result

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Bulk Text-to-Speech Results](actions/fetch-bulk-text-to-speech-results.md) | GET | Retrieves multiple text-to-speech results from CAMB.AI. |
| [Get Text-to-Speech Result](actions/get-text-to-speech-result.md) | GET | Retrieves a text-to-speech result from CAMB.AI. |

### Text-to-speech Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Text-to-Speech](actions/create-text-to-speech.md) | POST | Creates a new text-to-speech task in CAMB.AI. |

### Text-to-speech Task Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Text-to-Speech Task Status](actions/get-text-to-speech-task-status.md) | GET | Retrieves text-to-speech task status from CAMB.AI. |

### Translated Text-to-speech Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Translated Text-to-Speech](actions/create-translated-text-to-speech.md) | POST | Creates a translated text-to-speech task in CAMB.AI. |

### Translated Text-to-speech Task Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Translated Text-to-Speech Status](actions/get-translated-text-to-speech-status.md) | GET | Retrieves translated text-to-speech task status from CAMB.AI. |

### Translation Result

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Bulk Translation Results](actions/fetch-bulk-translation-results.md) | GET | Retrieves multiple translation results from CAMB.AI. |
| [Get Translation Result](actions/get-translation-result.md) | GET | Retrieves a translation result from CAMB.AI. |

### Translation Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Translation](actions/create-translation.md) | POST | Creates a new translation task in CAMB.AI. |

### Translation Task Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Translation Task Status](actions/get-translation-task-status.md) | GET | Retrieves translation task status from CAMB.AI. |

### Voice

| Action | Method | Description |
| --- | --- | --- |
| [List Voices](actions/list-voices.md) | GET | Retrieves all available voices from CAMB.AI. |

### Voice Generation Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Voice from Description Result](actions/get-voice-from-description-result.md) | GET | Retrieves a voice-from-description result from CAMB.AI. |

### Voice Generation Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Voice from Description](actions/create-voice-from-description.md) | POST | Creates a new voice from a description in CAMB.AI. |

### Voice Generation Task Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Voice from Description Task Status](actions/get-voice-from-description-task-status.md) | GET | Retrieves voice-from-description task status from CAMB.AI. |

