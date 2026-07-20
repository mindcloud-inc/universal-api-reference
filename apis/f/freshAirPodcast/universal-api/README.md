# <img src="https://images.mindcloud.co/apps/icons/fresh-air-podcast_1776453103678.png" alt="Fresh Air Podcast logo" width="28" height="28"> Fresh Air Podcast: Universal API

Official NPR Fresh Air podcast RSS feed. Use it to read the latest published episodes and feed metadata from the canonical public NPR feed.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/freshAirPodcast/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.npr.org/podcasts/381444908/fresh-air
- **Vendor API docs:** https://www.npr.org/podcasts/381444908/fresh-air

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Episodes](actions/list-episodes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshAirPodcast/latest/actions/list-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Episode

| Action | Method | Description |
| --- | --- | --- |
| [List Episodes](actions/list-episodes.md) | GET |  |

