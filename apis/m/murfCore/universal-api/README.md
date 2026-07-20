# <img src="https://images.mindcloud.co/apps/icons/murf-core_1774301510072.png" alt="Murf Core logo" width="28" height="28"> Murf Core: Universal API

Generate speech, transform audio, translate text, and manage voices

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/murfCore/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://murf.ai
- **Vendor API docs:** https://murf.ai/api/docs/introduction/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Voices](actions/list-voices.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/murfCore/latest/actions/list-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Speech

| Action | Method | Description |
| --- | --- | --- |
| [Synthesize Speech](actions/synthesize-speech.md) | POST | Synthesizes speech from text in Murf Core. |

### Translation

| Action | Method | Description |
| --- | --- | --- |
| [Translate Text](actions/translate-text.md) | POST | Translates text into another language with Murf Core. |

### Voice

| Action | Method | Description |
| --- | --- | --- |
| [List Voices](actions/list-voices.md) | GET | Retrieves available voices from Murf Core. |

### Voice Conversion

| Action | Method | Description |
| --- | --- | --- |
| [Voice Changer](actions/voice-changer.md) | POST | Converts audio to another voice with Murf Core. |

