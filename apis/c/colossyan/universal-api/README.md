# <img src="https://images.mindcloud.co/apps/icons/images-21_1774871510755.png" alt="Colossyan logo" width="28" height="28"> Colossyan: Universal API

Create and manage Colossyan video-generation jobs, generated videos, avatars, voices, and draft generation from knowledge inputs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/colossyan/latest
- **Category:** Communication / Video Communications
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.colossyan.com
- **Vendor API docs:** https://docs.colossyan.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Voices](actions/list-voices.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/list-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Avatar

| Action | Method | Description |
| --- | --- | --- |
| [Create Avatar](actions/create-avatar.md) | POST | Creates a new avatar in Colossyan. |
| [List Avatars](actions/list-avatars.md) | GET | Retrieves available avatars from Colossyan. |

### Draft

| Action | Method | Description |
| --- | --- | --- |
| [Generate Draft From Knowledge](actions/generate-draft-from-knowledge.md) | POST | Creates a draft from structured knowledge in Colossyan. |

### Generated Video

| Action | Method | Description |
| --- | --- | --- |
| [Delete Generated Video](actions/delete-generated-video.md) | DELETE | Deletes a generated video from Colossyan. |
| [Retrieve Generated Video](actions/retrieve-generated-video.md) | GET | Retrieves a generated video from Colossyan. |

### Template Video Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Video From Template](actions/create-video-from-template.md) | POST | Creates a video generation job from a Colossyan template. |

### Video Generation Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Video Generation Job](actions/create-video-generation-job.md) | POST | Creates a new video generation job in Colossyan. |
| [Delete Video Generation Job](actions/delete-video-generation-job.md) | DELETE | Deletes a video generation job from Colossyan. |
| [Retrieve Video Generation Job](actions/retrieve-video-generation-job.md) | GET | Retrieves a video generation job from Colossyan. |

### Voice

| Action | Method | Description |
| --- | --- | --- |
| [List Voices](actions/list-voices.md) | GET | Retrieves available voices from Colossyan. |

