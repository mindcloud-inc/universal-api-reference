# <img src="https://images.mindcloud.co/apps/icons/g-news_1776794822206.png" alt="GNews logo" width="28" height="28"> GNews: Universal API

Search news articles and track top headlines

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gNews/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://gnews.io
- **Vendor API docs:** https://docs.gnews.io

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Top Headlines](actions/list-top-headlines.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gNews/latest/actions/list-top-headlines?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Article

| Action | Method | Description |
| --- | --- | --- |
| [List Top Headlines](actions/list-top-headlines.md) | GET | Retrieves current top news headlines from GNews. |
| [Search Articles](actions/search-articles.md) | GET | Searches GNews for news articles by keyword. |

