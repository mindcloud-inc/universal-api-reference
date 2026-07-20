# <img src="https://images.mindcloud.co/apps/icons/uberduck-icon-512_1776260804431.png" alt="Uberduck logo" width="28" height="28"> Uberduck: Universal API

Generate text-to-speech audio, list voices, clone voices, and list speech models with the Uberduck API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/uberduck/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.uberduck.ai
- **Vendor API docs:** https://docs.uberduck.ai/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Models](actions/get-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uberduck/latest/actions/get-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Models](actions/get-models.md) | GET | Retrieves available TTS models from Uberduck. |
| [Instant Voice Clone](actions/instant-voice-clone.md) | POST | Creates a zero-shot voice in Uberduck. |
| [List Voices](actions/list-voices.md) | GET | Retrieves available voice options from Uberduck. |
| [Text To Speech](actions/text-to-speech.md) | POST | Creates speech audio in Uberduck from input text. |

