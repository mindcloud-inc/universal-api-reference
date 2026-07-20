# <img src="https://images.mindcloud.co/apps/icons/money-talks-news_1776442281286.png" alt="Money Talks News logo" width="28" height="28"> Money Talks News: Universal API

Reads syndicated article items from the Money Talks News RSS feed URL supplied in the selected connection.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/moneyTalksNews/latest
- **Category:** Website & App Building / CMS
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.moneytalksnews.com
- **Vendor API docs:** https://www.rssboard.org/rss-specification

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Site Feed Items](actions/list-site-feed-items.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moneyTalksNews/latest/actions/list-site-feed-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Rss Comment

| Action | Method | Description |
| --- | --- | --- |
| [List Global Comments Feed Items](actions/list-global-comments-feed-items.md) | GET |  |
| [List Post Comments Feed Items](actions/list-post-comments-feed-items.md) | GET |  |

### Rss Item

| Action | Method | Description |
| --- | --- | --- |
| [List Author Feed Items](actions/list-author-feed-items.md) | GET |  |
| [List Category Feed Items](actions/list-category-feed-items.md) | GET |  |
| [List Search Feed Items](actions/list-search-feed-items.md) | GET |  |
| [List Site Feed Items](actions/list-site-feed-items.md) | GET |  |
| [List Tag Feed Items](actions/list-tag-feed-items.md) | GET |  |

