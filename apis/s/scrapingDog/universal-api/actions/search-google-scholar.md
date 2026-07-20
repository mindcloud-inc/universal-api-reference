# ScrapingDog: Search Google Scholar

Retrieves Google Scholar search results through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-scholar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-scholar?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-scholar?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | Search query for Google Scholar. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "current": 1,
        "page_no": {
          "1": "string",
          "2": "string",
          "3": "string",
          "4": "string",
          "5": "string",
          "6": "string",
          "7": "string",
          "8": "string",
          "9": "string"
        }
      },
      "related_searches": {
        "link": "https://example.com",
        "title": "string"
      },
      "scholar_results": {
        "displayed_link": "https://example.com",
        "id": "string",
        "inline_links": {
          "cited_by": {
            "cites_id": "https://example.com",
            "link": "https://example.com",
            "total": "https://example.com"
          },
          "related_pages_link": "https://example.com",
          "versions": {
            "cluster_id": "https://example.com",
            "link": "https://example.com",
            "total": "https://example.com"
          }
        },
        "resources": {
          "link": "https://example.com",
          "title": "string",
          "type": "string"
        },
        "snippet": "string",
        "title": "string",
        "title_link": "https://example.com"
      },
      "scrapingdog_pagination": {
        "current": 1,
        "page_no": {
          "1": "string",
          "2": "string",
          "3": "string",
          "4": "string",
          "5": "string",
          "6": "string",
          "7": "string",
          "8": "string",
          "9": "string",
          "10": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination` | object |  |
| `pagination.current` | number |  |
| `pagination.page_no` | object |  |
| `pagination.page_no.1` | string |  |
| `pagination.page_no.2` | string |  |
| `pagination.page_no.3` | string |  |
| `pagination.page_no.4` | string |  |
| `pagination.page_no.5` | string |  |
| `pagination.page_no.6` | string |  |
| `pagination.page_no.7` | string |  |
| `pagination.page_no.8` | string |  |
| `pagination.page_no.9` | string |  |
| `related_searches` | array<object> |  |
| `related_searches.link` | string |  |
| `related_searches.title` | string |  |
| `scholar_results` | array<object> |  |
| `scholar_results.displayed_link` | string |  |
| `scholar_results.id` | string |  |
| `scholar_results.inline_links` | object |  |
| `scholar_results.inline_links.cited_by` | object |  |
| `scholar_results.inline_links.cited_by.cites_id` | string |  |
| `scholar_results.inline_links.cited_by.link` | string |  |
| `scholar_results.inline_links.cited_by.total` | string |  |
| `scholar_results.inline_links.related_pages_link` | string |  |
| `scholar_results.inline_links.versions` | object |  |
| `scholar_results.inline_links.versions.cluster_id` | string |  |
| `scholar_results.inline_links.versions.link` | string |  |
| `scholar_results.inline_links.versions.total` | string |  |
| `scholar_results.resources` | array<object> |  |
| `scholar_results.resources.link` | string |  |
| `scholar_results.resources.title` | string |  |
| `scholar_results.resources.type` | string |  |
| `scholar_results.snippet` | string |  |
| `scholar_results.title` | string |  |
| `scholar_results.title_link` | string |  |
| `scrapingdog_pagination` | object |  |
| `scrapingdog_pagination.current` | number |  |
| `scrapingdog_pagination.page_no` | object |  |
| `scrapingdog_pagination.page_no.1` | string |  |
| `scrapingdog_pagination.page_no.10` | string |  |
| `scrapingdog_pagination.page_no.2` | string |  |
| `scrapingdog_pagination.page_no.3` | string |  |
| `scrapingdog_pagination.page_no.4` | string |  |
| `scrapingdog_pagination.page_no.5` | string |  |
| `scrapingdog_pagination.page_no.6` | string |  |
| `scrapingdog_pagination.page_no.7` | string |  |
| `scrapingdog_pagination.page_no.8` | string |  |
| `scrapingdog_pagination.page_no.9` | string |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google_scholar` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google-scholar.md) for the provider-specific parameters and requirements.

