# <img src="https://images.mindcloud.co/apps/icons/quanta-science-podcast_1776431408232.png" alt="Quanta Science Podcast logo" width="28" height="28"> Quanta Science Podcast: Universal API

Browse Quanta podcast episodes and audio links

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/quantaSciencePodcast/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.quantamagazine.org
- **Vendor API docs:** https://www.quantamagazine.org/tag/quanta-podcast/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Podcast Episodes](actions/list-podcast-episodes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quantaSciencePodcast/latest/actions/list-podcast-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Podcast Episode

| Action | Method | Description |
| --- | --- | --- |
| [List Podcast Episodes](actions/list-podcast-episodes.md) | GET |  |

