# ScrapingDog: Search DuckDuckGo

Retrieves DuckDuckGo search results through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-duck-duck-go
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-duck-duck-go?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-duck-duck-go?${params}`, {
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
| `query` | string | yes | Search query for DuckDuckGo. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "next_page_token": "string",
      "organic_results": {
        "displayed_link": "https://example.com",
        "link": "https://example.com",
        "rank": 1,
        "snippet": "string",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `next_page_token` | string |  |
| `organic_results` | array<object> |  |
| `organic_results.displayed_link` | string |  |
| `organic_results.link` | string |  |
| `organic_results.rank` | number |  |
| `organic_results.snippet` | string |  |
| `organic_results.title` | string |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /duckduckgo/search` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-duck-duck-go.md) for the provider-specific parameters and requirements.

