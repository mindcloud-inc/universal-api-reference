# <img src="https://images.mindcloud.co/apps/icons/type-cast_1775750026252.png" alt="TypeCast logo" width="28" height="28"> TypeCast: Universal API

Generate speech, stream audio, and inspect TypeCast voices

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/typeCast/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://typecast.ai
- **Vendor API docs:** https://typecast.ai/docs/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Subscription](actions/get-subscription.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typeCast/latest/actions/get-subscription?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Audio File

| Action | Method | Description |
| --- | --- | --- |
| [Streaming Text To Speech](actions/streaming-text-to-speech.md) | POST | Creates streaming speech audio in TypeCast. |
| [Text To Speech](actions/text-to-speech.md) | POST | Creates a speech audio file in TypeCast. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscription](actions/get-subscription.md) | GET | Retrieves current subscription details from TypeCast. |

### Voice

| Action | Method | Description |
| --- | --- | --- |
| [Get Voice Details](actions/get-voice-details.md) | GET | Retrieves details for a specific voice from TypeCast. |
| [List Voices](actions/list-voices.md) | GET | Retrieves available voices from TypeCast. |

