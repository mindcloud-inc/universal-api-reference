# <img src="https://images.mindcloud.co/apps/icons/t-edradio-hour-podcast_1776454017770.png" alt="TED Radio Hour Podcast logo" width="28" height="28"> TED Radio Hour Podcast: Universal API

Browse TED Radio Hour episodes and podcast metadata from NPR

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tEDRadioHourPodcast/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.npr.org/podcasts/510298/ted-radio-hour
- **Vendor API docs:** https://www.npr.org/podcasts/510298/ted-radio-hour

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Episodes](actions/list-episodes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tEDRadioHourPodcast/latest/actions/list-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Episodes

| Action | Method | Description |
| --- | --- | --- |
| [List Episodes](actions/list-episodes.md) | GET | Retrieves episodes from the TED Radio Hour Podcast. |

