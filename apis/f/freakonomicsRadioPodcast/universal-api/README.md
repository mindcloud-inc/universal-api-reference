# <img src="https://images.mindcloud.co/apps/icons/freakonomics-radio-podcast_1776694311541.png" alt="Freakonomics Radio Podcast logo" width="28" height="28"> Freakonomics Radio Podcast: Universal API

Read public episode and show metadata from the official Freakonomics Radio RSS feed.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/freakonomicsRadioPodcast/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://freakonomics.com
- **Vendor API docs:** https://feeds.simplecast.com/Y8lFbOT4

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Episodes](actions/list-episodes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freakonomicsRadioPodcast/latest/actions/list-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Episode

| Action | Method | Description |
| --- | --- | --- |
| [List Episodes](actions/list-episodes.md) | GET | Retrieves episodes from the Freakonomics Radio RSS feed. |

