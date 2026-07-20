# <img src="https://images.mindcloud.co/apps/icons/vadootv_1776785901449.png" alt="Vadootv logo" width="28" height="28"> Vadootv: Universal API

Vadoo AI API for generating videos, captions, clips, podcasts, and AI character imagery from text or media inputs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vadootv/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.vadoo.tv/
- **Vendor API docs:** https://docs.vadoo.tv/docs/intro/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get my balance](actions/get-my-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/get-my-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Ai Character

| Action | Method | Description |
| --- | --- | --- |
| [Get all characters](actions/get-all-characters.md) | GET | Retrieves AI characters from Vadootv. |

### Ai Clips Job

| Action | Method | Description |
| --- | --- | --- |
| [Create AI clips](actions/create-ai-clips.md) | POST | Creates an AI clips job in Vadootv. |

### Ai Podcast

| Action | Method | Description |
| --- | --- | --- |
| [Generate podcast](actions/generate-podcast.md) | POST | Creates an AI podcast in Vadootv. |

### Ai Video

| Action | Method | Description |
| --- | --- | --- |
| [Generate video](actions/generate-video.md) | POST | Creates an AI video in Vadootv. |

### Background Music

| Action | Method | Description |
| --- | --- | --- |
| [Get background music](actions/get-background-music.md) | GET | Retrieves available background music tracks from Vadootv. |

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get my balance](actions/get-my-balance.md) | GET | Retrieves your current credit balance from Vadootv. |

### Captioned Video

| Action | Method | Description |
| --- | --- | --- |
| [Add captions](actions/add-captions.md) | POST | Creates a captioned video in Vadootv. |

### Character Image

| Action | Method | Description |
| --- | --- | --- |
| [Get character image](actions/get-character-image.md) | GET | Retrieves a generated character image URL from Vadootv. |

### Character Image Job

| Action | Method | Description |
| --- | --- | --- |
| [Generate character image](actions/generate-character-image.md) | POST | Creates a character image in Vadootv. |

### Language

| Action | Method | Description |
| --- | --- | --- |
| [Get languages](actions/get-languages.md) | GET | Retrieves supported languages from Vadootv. |

### Style

| Action | Method | Description |
| --- | --- | --- |
| [Get styles](actions/get-styles.md) | GET | Retrieves available video styles from Vadootv. |

### Theme

| Action | Method | Description |
| --- | --- | --- |
| [Get themes](actions/get-themes.md) | GET | Retrieves available caption themes from Vadootv. |

### Topic

| Action | Method | Description |
| --- | --- | --- |
| [Get topics](actions/get-topics.md) | GET | Retrieves available video topics from Vadootv. |

### Video Render

| Action | Method | Description |
| --- | --- | --- |
| [Get video URL](actions/get-video-url.md) | GET | Retrieves a generated video URL from Vadootv. |

### Voice

| Action | Method | Description |
| --- | --- | --- |
| [Get voices](actions/get-voices.md) | GET | Retrieves available AI voices from Vadootv. |

