# <img src="https://images.mindcloud.co/apps/icons/code-switch-tile-npr-network-01-sq-d238b5cbd3882f82ea3253c4facbe1f6fc9a78a1_1776451870057.jpeg" alt="Code Switch Podcast logo" width="28" height="28"> Code Switch Podcast: Universal API

Official NPR Code Switch podcast RSS feed.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/codeSwitchPodcast/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.npr.org/podcasts/510312/codeswitch
- **Vendor API docs:** https://www.npr.org/podcasts/510312/codeswitch

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Podcast Feed](actions/get-podcast-feed.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeSwitchPodcast/latest/actions/get-podcast-feed?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Podcast Feed

| Action | Method | Description |
| --- | --- | --- |
| [Get Podcast Feed](actions/get-podcast-feed.md) | GET | Retrieves the Code Switch podcast RSS feed from NPR. |

