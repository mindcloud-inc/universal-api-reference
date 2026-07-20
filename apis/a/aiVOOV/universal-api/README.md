# <img src="https://images.mindcloud.co/apps/icons/ai-voov_1775491609463.png" alt="AiVOOV logo" width="28" height="28"> AiVOOV: Universal API

Generate speech and list AI voices

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aiVOOV/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://aivoov.com
- **Vendor API docs:** https://documenter.getpostman.com/view/5434397/2sB2qXki3a

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Voices](actions/list-voices.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aiVOOV/latest/actions/list-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Audio

| Action | Method | Description |
| --- | --- | --- |
| [Create Audio](actions/create-audio.md) | POST | Creates audio from multiple voice and text inputs in AiVOOV. |

### Voice

| Action | Method | Description |
| --- | --- | --- |
| [List Voices](actions/list-voices.md) | GET | Retrieves available voice IDs from AiVOOV. |

