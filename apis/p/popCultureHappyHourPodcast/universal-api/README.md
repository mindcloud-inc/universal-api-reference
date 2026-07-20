# <img src="https://images.mindcloud.co/apps/icons/pop-culture-happy-hour-podcast_1776371362855.png" alt="Pop Culture Happy Hour Podcast logo" width="28" height="28"> Pop Culture Happy Hour Podcast: Universal API

NPR Pop Culture Happy Hour podcast RSS feed.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/popCultureHappyHourPodcast/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.npr.org/podcasts/510282/pop-culture-happy-hour
- **Vendor API docs:** https://www.npr.org/podcasts/510282/pop-culture-happy-hour

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Recent Episodes](actions/list-recent-episodes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/popCultureHappyHourPodcast/latest/actions/list-recent-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [List Recent Episodes](actions/list-recent-episodes.md) | GET | Retrieves recent podcast episodes from Pop Culture Happy Hour Podcast. |

