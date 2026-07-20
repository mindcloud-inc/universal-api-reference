# <img src="https://images.mindcloud.co/apps/icons/news-api_1776114017603.png" alt="News API logo" width="28" height="28"> News API: Universal API

Search breaking news headlines, source metadata, and historical articles from News API's REST endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/newsAPI/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://newsapi.org
- **Vendor API docs:** https://newsapi.org/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sources](actions/list-sources.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsAPI/latest/actions/list-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Data Sources

| Action | Method | Description |
| --- | --- | --- |
| [List Sources](actions/list-sources.md) | GET | Retrieves top-headline news sources from News API. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [List Top Headlines](actions/list-top-headlines.md) | GET | Finds top headlines in News API by country, category, or source. |
| [Search Everything](actions/search-everything.md) | GET | Finds articles in News API by keyword or phrase. |

