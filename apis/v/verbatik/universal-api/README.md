# <img src="https://images.mindcloud.co/apps/icons/verbatik_1775746321305.png" alt="Verbatik logo" width="28" height="28"> Verbatik: Universal API

Generate speech, clone voices, and create music

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/verbatik/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://verbatik.com
- **Vendor API docs:** https://docs.verbatik.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Voices](actions/list-voices.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verbatik/latest/actions/list-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Audio File

| Action | Method | Description |
| --- | --- | --- |
| [Upload Audio](actions/upload-audio.md) | POST | Uploads audio for Verbatik voice cloning. |

### Custom Voice Audio

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Voice Speech](actions/create-custom-voice-speech.md) | POST | Creates speech from a cloned voice in Verbatik. |

### Designed Voice

| Action | Method | Description |
| --- | --- | --- |
| [Create Voice Design](actions/create-voice-design.md) | POST | Creates a designed voice in Verbatik. |

### Music Audio

| Action | Method | Description |
| --- | --- | --- |
| [Create Music](actions/create-music.md) | POST | Creates music audio from text in Verbatik. |

### Speech Audio

| Action | Method | Description |
| --- | --- | --- |
| [Create Speech](actions/create-speech.md) | POST | Creates speech audio from text in Verbatik. |

### Voice

| Action | Method | Description |
| --- | --- | --- |
| [List My Voices](actions/list-my-voices.md) | GET | Retrieves your cloned voices from Verbatik. |
| [List Voices](actions/list-voices.md) | GET | Retrieves a list of voices from Verbatik. |

### Voice Clone

| Action | Method | Description |
| --- | --- | --- |
| [Create Voice Clone](actions/create-voice-clone.md) | POST | Creates a cloned voice in Verbatik. |

