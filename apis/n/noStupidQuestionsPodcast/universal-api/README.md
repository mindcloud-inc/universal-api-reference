# <img src="https://images.mindcloud.co/apps/icons/nsq-png-icon_1776448698649.jpeg" alt="No Stupid Questions Podcast logo" width="28" height="28"> No Stupid Questions Podcast: Universal API

Read public episode and show metadata from the No Stupid Questions podcast RSS feed.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/noStupidQuestionsPodcast/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://freakonomics.com/series/nsq/
- **Vendor API docs:** https://feeds.simplecast.com/dfh_verV

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Episodes](actions/list-episodes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/noStupidQuestionsPodcast/latest/actions/list-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Episode

| Action | Method | Description |
| --- | --- | --- |
| [List Episodes](actions/list-episodes.md) | GET | Retrieves podcast episodes from No Stupid Questions Podcast. |

