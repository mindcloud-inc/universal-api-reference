# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-17-as-10_1776432100597.png" alt="Creator Science Podcast logo" width="28" height="28"> Creator Science Podcast: Universal API

List Creator Science podcast episodes

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/creatorSciencePodcast/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://podcast.creatorscience.com
- **Vendor API docs:** https://podcast.creatorscience.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Podcast Episodes](actions/list-podcast-episodes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/creatorSciencePodcast/latest/actions/list-podcast-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Podcast Episode

| Action | Method | Description |
| --- | --- | --- |
| [List Podcast Episodes](actions/list-podcast-episodes.md) | GET | Retrieves podcast episodes from the Creator Science Podcast feed. |

