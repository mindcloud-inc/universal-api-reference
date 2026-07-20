# <img src="https://images.mindcloud.co/apps/icons/hume-ai_1782742979963.png" alt="Hume AI logo" width="28" height="28"> Hume AI: Universal API

Generate speech, build voice agents, and manage voice assets

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/humeAI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.hume.ai/
- **Vendor API docs:** https://dev.hume.ai/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Configs](actions/list-configs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/list-configs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Config

| Action | Method | Description |
| --- | --- | --- |
| [Create Config](actions/create-config.md) | POST | Creates a new EVI config in Hume AI. |
| [Delete Config](actions/delete-config.md) | DELETE | Deletes an existing EVI config from Hume AI. |
| [Get Config](actions/get-config.md) | GET |  |
| [List Configs](actions/list-configs.md) | GET | Retrieves EVI configs from Hume AI. |
| [Update Config](actions/update-config.md) | PUT |  |

### Prompt

| Action | Method | Description |
| --- | --- | --- |
| [Create Prompt](actions/create-prompt.md) | POST | Creates a new EVI prompt in Hume AI. |
| [Delete Prompt](actions/delete-prompt.md) | DELETE | Deletes an existing EVI prompt from Hume AI. |
| [Get Prompt](actions/get-prompt.md) | GET |  |
| [List Prompts](actions/list-prompts.md) | GET | Retrieves EVI prompts from Hume AI. |
| [Update Prompt](actions/update-prompt.md) | PUT |  |

### Speech

| Action | Method | Description |
| --- | --- | --- |
| [Stream Speech File](actions/stream-speech-file.md) | POST | Streams synthesized speech from Hume AI as an audio file. |
| [Stream Speech JSON](actions/stream-speech-json.md) | POST | Streams synthesized speech from Hume AI as JSON. |
| [Synthesize Speech File](actions/synthesize-speech-file.md) | POST | Synthesizes speech in Hume AI and returns an audio file. |
| [Synthesize Speech JSON](actions/synthesize-speech-json.md) | POST | Synthesizes speech in Hume AI and returns JSON audio. |

### Tool

| Action | Method | Description |
| --- | --- | --- |
| [Create Tool](actions/create-tool.md) | POST | Creates a new EVI tool in Hume AI. |
| [Delete Tool](actions/delete-tool.md) | DELETE | Deletes an existing EVI tool from Hume AI. |
| [Get Tool](actions/get-tool.md) | GET |  |
| [List Tools](actions/list-tools.md) | GET | Retrieves EVI tools from Hume AI. |
| [Update Tool](actions/update-tool.md) | PUT |  |

### Voice

| Action | Method | Description |
| --- | --- | --- |
| [Convert Voice File](actions/convert-voice-file.md) | POST | Converts uploaded audio in Hume AI and returns a streamed audio file. |
| [Convert Voice JSON](actions/convert-voice-json.md) | POST | Converts uploaded audio in Hume AI and returns streamed JSON. |
| [Create Voice](actions/create-voice.md) | POST | Creates a custom voice in Hume AI. |
| [Delete Voice](actions/delete-voice.md) | DELETE | Deletes an existing custom voice from Hume AI. |
| [List Voices](actions/list-voices.md) | GET | Retrieves voices from Hume AI. |

