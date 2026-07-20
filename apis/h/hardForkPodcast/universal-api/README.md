# <img src="https://images.mindcloud.co/apps/icons/hard-fork-podcast_1776443969552.png" alt="Hard Fork Podcast logo" width="28" height="28"> Hard Fork Podcast: Universal API

Public RSS feed wrapper for The New York Times Hard Fork podcast. Use it to read the latest published episodes and episode metadata from the official Simplecast feed.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hardForkPodcast/latest
- **Category:** Website & App Building / CMS
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.nytimes.com/column/hard-fork
- **Vendor API docs:** https://feeds.simplecast.com/6HKOhNgS

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Episodes](actions/list-episodes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hardForkPodcast/latest/actions/list-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Episode

| Action | Method | Description |
| --- | --- | --- |
| [List Episodes](actions/list-episodes.md) | GET | Retrieves podcast episodes from Hard Fork Podcast. |

