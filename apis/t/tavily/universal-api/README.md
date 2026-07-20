# <img src="https://images.mindcloud.co/apps/icons/tavily_1773934419902.png" alt="Tavily logo" width="28" height="28"> Tavily: Universal API

Search, extract, crawl, map, and research web content

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tavily/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tavily.com
- **Vendor API docs:** https://docs.tavily.com/documentation/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Web](actions/search-web.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tavily/latest/actions/search-web?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Content Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Extract Content](actions/extract-content.md) | GET | Retrieves web page content from URLs with Tavily. |

### Research Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Research Task](actions/create-research-task.md) | POST | Creates a research task in Tavily. |
| [Get Research Task Status](actions/get-research-task-status.md) | GET | Retrieves Tavily research task status and results by request ID. |

### Search

| Action | Method | Description |
| --- | --- | --- |
| [Search Web](actions/search-web.md) | GET | Finds web search results in Tavily by query. |

### Site Crawl

| Action | Method | Description |
| --- | --- | --- |
| [Crawl Site](actions/crawl-site.md) | GET | Crawls a website from a base URL with Tavily. |

### Site Map

| Action | Method | Description |
| --- | --- | --- |
| [Map Site](actions/map-site.md) | GET | Maps a website from a base URL with Tavily. |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage](actions/get-usage.md) | GET | Retrieves API key and account usage details from Tavily. |

