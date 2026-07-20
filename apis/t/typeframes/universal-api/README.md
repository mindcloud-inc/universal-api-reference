# <img src="https://images.mindcloud.co/apps/icons/typeframes_1776178844727.png" alt="Typeframes logo" width="28" height="28"> Typeframes: Universal API

Create and manage AI-generated videos in Revid AI. Render videos from scripts, prompts, audio, articles, avatars, static backgrounds, and motion transfer workflows; estimate credits; track projects; publish and export renders; and manage consistent characters and cloned voices.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/typeframes/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.revid.ai
- **Vendor API docs:** https://documenter.getpostman.com/view/36975521/2sBXcGEfaB

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Projects](actions/get-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typeframes/latest/actions/get-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Projects](actions/get-projects.md) | GET | Retrieves recent video projects from Typeframes. |

