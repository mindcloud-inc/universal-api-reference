# <img src="https://images.mindcloud.co/apps/icons/news-dataio_1776872255005.png" alt="NewsData.io logo" width="28" height="28"> NewsData.io: Universal API

NewsData.io provides real-time, historical, crypto, market, and source-metadata news APIs backed by a single API key.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/newsDataio/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://newsdata.io
- **Vendor API docs:** https://newsdata.io/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Latest News](actions/list-latest-news.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsDataio/latest/actions/list-latest-news?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Archived News Article

| Action | Method | Description |
| --- | --- | --- |
| [List Archived News](actions/list-archived-news.md) | GET |  |

### Crypto News Article

| Action | Method | Description |
| --- | --- | --- |
| [List Crypto News](actions/list-crypto-news.md) | GET |  |

### Crypto News Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Crypto News](actions/count-crypto-news.md) | GET |  |

### Market News Article

| Action | Method | Description |
| --- | --- | --- |
| [List Market News](actions/list-market-news.md) | GET |  |

### Market News Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Market News](actions/count-market-news.md) | GET |  |

### News Article

| Action | Method | Description |
| --- | --- | --- |
| [List Latest News](actions/list-latest-news.md) | GET |  |

### News Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Archived News](actions/count-archived-news.md) | GET |  |

### News Source

| Action | Method | Description |
| --- | --- | --- |
| [List News Sources](actions/list-news-sources.md) | GET |  |

