# <img src="https://images.mindcloud.co/apps/icons/favicon-app-fliz-ai-48x48_1778082825175.png" alt="Fliz logo" width="28" height="28"> Fliz: Universal API

Fliz is an AI video creation platform for generating, listing, retrieving, translating, and managing videos programmatically.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fliz/latest
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://fliz.ai/
- **Vendor API docs:** https://app.fliz.ai/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get video](actions/get-video.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fliz/latest/actions/get-video?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Music

| Action | Method | Description |
| --- | --- | --- |
| [List musics](actions/list-musics.md) | GET | Retrieves available background music tracks from Fliz. |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Create video](actions/create-video.md) | POST | Creates a new video in Fliz. |
| [Get video](actions/get-video.md) | GET | Retrieves a video from your Fliz account. |
| [List videos](actions/list-videos.md) | GET | Retrieves videos from your Fliz account. |
| [Translate video](actions/translate-video.md) | POST | Creates a translated video in Fliz. |

### Voice

| Action | Method | Description |
| --- | --- | --- |
| [List voices](actions/list-voices.md) | GET | Retrieves available text-to-speech voices from Fliz. |

