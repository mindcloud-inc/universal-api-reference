# Firecrawl: Search Web

Finds web results with Firecrawl.

```
GET https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/search-web
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firecrawl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/search-web?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/search-web?${params}`, {
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
| `query` | string | yes | The search query |
| `limit` | number | no | Maximum number of results to return |
| `sources[]` | array<object> | no | Sources to search |
| `categories[]` | array<object> | no | Categories to filter results by |
| `tbs` | string | no | Time-based search parameter |
| `location` | string | no | Location parameter for search results |
| `country` | string | no | ISO country code for geo-targeting search results |
| `timeout` | number | no | Timeout in milliseconds |
| `ignoreInvalidURLs` | boolean | no | Exclude URLs that are invalid for other Firecrawl endpoints |
| `scrapeOptions` | object | no | Options for scraping search results |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "id": "string",
      "web": {
        "description": "string",
        "position": 1,
        "title": "string",
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsUsed` | number |  |
| `id` | string |  |
| `web` | array<object> |  |
| `web.description` | string |  |
| `web.position` | number |  |
| `web.title` | string |  |
| `web.url` | string |  |

## Native endpoint

Through the native Firecrawl API, this operation is `POST /search` (base URL `https://api.firecrawl.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-web.md) for the provider-specific parameters and requirements.

