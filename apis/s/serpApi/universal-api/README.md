# <img src="https://images.mindcloud.co/apps/icons/serp-api_1774539354166.png" alt="SerpApi logo" width="28" height="28"> SerpApi: Universal API

SerpApi provides structured search engine results and related search APIs across Google, Bing, Amazon, YouTube, and other supported engines.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/serpApi/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://serpapi.com
- **Vendor API docs:** https://serpapi.com/search-engine-apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Google](actions/search-google.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serpApi/latest/actions/search-google?connectionId=$CONNECTION_ID&limit=25&offset=0&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Ai Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Google AI Mode](actions/search-google-ai-mode.md) | GET | Retrieves Google AI Mode results from SerpApi. |
| [Search Google AI Overview](actions/search-google-ai-overview.md) | GET | Retrieves Google AI Overview results from SerpApi. |

### Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Google Events](actions/search-google-events.md) | GET | Retrieves Google event results from SerpApi. |

### Finance Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Google Finance](actions/search-google-finance.md) | GET | Retrieves Google Finance results from SerpApi. |

### Forum Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Google Forums](actions/search-google-forums.md) | GET | Retrieves Google forum results from SerpApi. |

### Image Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Bing Images](actions/search-bing-images.md) | GET | Retrieves Bing image results from SerpApi. |
| [Search Google Images](actions/search-google-images.md) | GET | Retrieves Google image results from SerpApi. |

### Job Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Google Jobs](actions/search-google-jobs.md) | GET | Retrieves Google job results from SerpApi. |

### Local Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Google Local](actions/search-google-local.md) | GET | Retrieves Google local results from SerpApi. |

### Map Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Google Maps](actions/search-google-maps.md) | GET | Retrieves Google Maps results from SerpApi. |

### News Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Google News](actions/search-google-news.md) | GET | Retrieves Google News results from SerpApi. |

### Patent Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Google Patents](actions/search-google-patents.md) | GET | Retrieves Google patent results from SerpApi. |

### Product Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Google Shopping](actions/search-google-shopping.md) | GET | Retrieves Google Shopping results from SerpApi. |

### Scholar Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Google Scholar](actions/search-google-scholar.md) | GET | Retrieves Google Scholar results from SerpApi. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Bing Web](actions/search-bing-web.md) | GET | Retrieves Bing web search results from SerpApi. |
| [Search DuckDuckGo Light](actions/search-duckduckgo-light.md) | GET | Retrieves DuckDuckGo Light search results from SerpApi. |
| [Search DuckDuckGo Web](actions/search-duckduckgo-web.md) | GET | Retrieves DuckDuckGo web search results from SerpApi. |
| [Search Google](actions/search-google.md) | GET | Retrieves Google search results from SerpApi. |
| [Search Google Light](actions/search-google-light.md) | GET | Retrieves Google Light search results from SerpApi. |
| [Search Yahoo Web](actions/search-yahoo-web.md) | GET | Retrieves Yahoo web search results from SerpApi. |

### Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Google](actions/autocomplete-google.md) | GET | Retrieves Google autocomplete suggestions from SerpApi. |

### Trend Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Google Trends](actions/search-google-trends.md) | GET | Retrieves Google Trends results from SerpApi. |

### Video Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Google Videos](actions/search-google-videos.md) | GET | Retrieves Google video results from SerpApi. |
| [Search YouTube](actions/search-youtube.md) | GET | Retrieves YouTube search results from SerpApi. |

