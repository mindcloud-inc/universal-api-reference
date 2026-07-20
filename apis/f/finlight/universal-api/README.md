# <img src="https://images.mindcloud.co/apps/icons/images_1774972227876.jpeg" alt="finlight logo" width="28" height="28"> finlight: Universal API

Retrieve real-time financial news, article lookups, source lists, and sentiment-enriched article data from Finlight.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/finlight/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://finlight.me/
- **Vendor API docs:** https://docs.finlight.me/v2/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sources](actions/list-sources.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finlight/latest/actions/list-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Article

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Article By Link](actions/fetch-article-by-link.md) | GET | Retrieves a single finlight article by URL. |
| [Fetch Articles](actions/fetch-articles.md) | GET | Finds financial news articles in finlight. |

### Source

| Action | Method | Description |
| --- | --- | --- |
| [List Sources](actions/list-sources.md) | GET | Retrieves supported news sources from finlight. |

