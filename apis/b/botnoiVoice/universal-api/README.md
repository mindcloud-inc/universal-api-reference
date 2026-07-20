# <img src="https://images.mindcloud.co/apps/icons/botnoi-voice_1775846495693.png" alt="Botnoi Voice logo" width="28" height="28"> Botnoi Voice: Universal API

Create speech audio and browse Botnoi Voice speakers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/botnoiVoice/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://voice.botnoi.ai
- **Vendor API docs:** https://voice.botnoi.ai/developer/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Speakers](actions/list-speakers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botnoiVoice/latest/actions/list-speakers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Audio

| Action | Method | Description |
| --- | --- | --- |
| [Generate Audio V1](actions/generate-audio-v1.md) | POST | Generates audio with Botnoi Voice V1. |
| [Generate Audio V2](actions/generate-audio-v2.md) | POST | Generates audio with Botnoi Voice V2. |

### Speaker

| Action | Method | Description |
| --- | --- | --- |
| [List Speakers](actions/list-speakers.md) | GET | Retrieves speakers from Botnoi Voice V2. |
| [List Speakers V1](actions/list-speakers-v1.md) | GET | Retrieves speakers from Botnoi Voice V1. |

