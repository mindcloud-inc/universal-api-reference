# <img src="https://images.mindcloud.co/apps/icons/idkuhvv8x-logos_1776715981904.jpeg" alt="Pipio logo" width="28" height="28"> Pipio: Universal API

List Pipio actors and voices and generate avatar videos

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pipio/latest
- **Category:** Communication / Video Communications
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pipio.ai
- **Vendor API docs:** https://docs.pipio.ai

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Languages](actions/list-languages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipio/latest/actions/list-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Avatar

| Action | Method | Description |
| --- | --- | --- |
| [List Avatars](actions/list-avatars.md) | GET | Finds available digital avatars in Pipio. |

### Ethnicity

| Action | Method | Description |
| --- | --- | --- |
| [List Ethnicities](actions/list-ethnicities.md) | GET | Finds supported avatar ethnicities in Pipio. |

### Language

| Action | Method | Description |
| --- | --- | --- |
| [List Languages](actions/list-languages.md) | GET | Finds supported voice languages in Pipio. |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Generate Dubbed Video Legacy](actions/generate-dubbed-video-legacy.md) | POST | Creates a dubbed video in Pipio using the legacy workflow. |
| [Generate Dubbed Video V2](actions/generate-dubbed-video-v2.md) | POST | Creates a dubbed video in Pipio using the v2 workflow. |
| [Generate Lip Sync Video](actions/generate-lip-sync-video.md) | POST | Creates a lip-synced video in Pipio from source video and audio. |
| [Generate Single Clip Video](actions/generate-single-clip-video.md) | POST | Creates a single-clip video in Pipio. |
| [List Videos](actions/list-videos.md) | GET | Finds all generated videos in Pipio. |
| [Retrieve Video](actions/retrieve-video.md) | GET | Retrieves a generated video from Pipio. |

### Voice

| Action | Method | Description |
| --- | --- | --- |
| [List Voices](actions/list-voices.md) | GET | Finds available voice options in Pipio. |

