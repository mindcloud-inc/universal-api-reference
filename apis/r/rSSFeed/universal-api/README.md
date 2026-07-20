# <img src="https://images.mindcloud.co/apps/icons/r-ssfeed_1776436589471.png" alt="RSS Feed logo" width="28" height="28"> RSS Feed: Universal API

Read and parse RSS 2.0 feeds from a user-supplied feed URL. RSS is a public XML syndication format published by the RSS Advisory Board.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rSSFeed/latest
- **Category:** Website & App Building / CMS
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.rssboard.org
- **Vendor API docs:** https://www.rssboard.org/rss-specification

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Feed Items](actions/list-feed-items.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rSSFeed/latest/actions/list-feed-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Rss Item

| Action | Method | Description |
| --- | --- | --- |
| [List Feed Items](actions/list-feed-items.md) | GET | Retrieves items from the configured RSS feed. |

