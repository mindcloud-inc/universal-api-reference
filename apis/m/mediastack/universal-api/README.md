# <img src="https://images.mindcloud.co/apps/icons/mediastack-icon_1777560228217.png" alt="Mediastack logo" width="28" height="28"> Mediastack: Universal API

Access worldwide live and historical news articles and news-source metadata from Mediastack's REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mediastack/latest
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mediastack.com
- **Vendor API docs:** https://mediastack.com/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search News](actions/search-news.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mediastack/latest/actions/search-news?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### News Article

| Action | Method | Description |
| --- | --- | --- |
| [Search Historical News](actions/search-historical-news.md) | GET | Finds historical news articles in Mediastack. |
| [Search News](actions/search-news.md) | GET | Finds news articles in Mediastack. |

### News Source

| Action | Method | Description |
| --- | --- | --- |
| [Search News Sources](actions/search-news-sources.md) | GET | Finds news sources in Mediastack. |

