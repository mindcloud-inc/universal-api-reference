# <img src="https://images.mindcloud.co/apps/icons/consider-this-podcast_1776442878019.png" alt="Consider This Podcast logo" width="28" height="28"> Consider This Podcast: Universal API

Read the latest Consider This from NPR episodes and episode metadata from the public podcast feed.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/considerThisPodcast/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.npr.org
- **Vendor API docs:** https://www.npr.org/podcasts/510355/considerthis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Episodes](actions/list-episodes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/considerThisPodcast/latest/actions/list-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Recordings

| Action | Method | Description |
| --- | --- | --- |
| [List Episodes](actions/list-episodes.md) | GET | Retrieves podcast episodes from Consider This Podcast. |

