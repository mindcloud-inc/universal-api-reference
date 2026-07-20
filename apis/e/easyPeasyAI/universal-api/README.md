# <img src="https://images.mindcloud.co/apps/icons/easy-peasy-ai_1774543461771.png" alt="Easy-Peasy.AI logo" width="28" height="28"> Easy-Peasy.AI: Universal API

All-in-one AI platform for text generation, image generation, video generation, transcription, text-to-speech, sound effects, chat completions, and bot conversations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/easyPeasyAI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://easy-peasy.ai
- **Vendor API docs:** https://docs.easy-peasy.ai

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Presets](actions/list-presets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyPeasyAI/latest/actions/list-presets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Chat

| Action | Method | Description |
| --- | --- | --- |
| [Chat Completions](actions/chat-completions.md) | POST | Creates a chat completion in Easy-Peasy.AI. |

### Sound

| Action | Method | Description |
| --- | --- | --- |
| [Generate Sound Effect](actions/generate-sound-effect.md) | POST | Generates a sound effect in Easy-Peasy.AI. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [List Presets](actions/list-presets.md) | GET | Retrieves text generation presets from Easy-Peasy.AI. |

### Text

| Action | Method | Description |
| --- | --- | --- |
| [Generate Text](actions/generate-text.md) | POST | Generates text in Easy-Peasy.AI from a preset. |
| [Generate Text-to-Speech](actions/generate-text-to-speech.md) | POST | Generates speech audio in Easy-Peasy.AI from text. |

### Tts

| Action | Method | Description |
| --- | --- | --- |
| [Get TTS Configuration](actions/get-tts-configuration.md) | GET | Retrieves TTS voice configuration from Easy-Peasy.AI. |
| [Get TTS Voices](actions/get-tts-voices.md) | GET | Retrieves TTS voices from Easy-Peasy.AI. |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Generate Talking Video](actions/generate-talking-video.md) | POST | Generates a talking video in Easy-Peasy.AI. |

