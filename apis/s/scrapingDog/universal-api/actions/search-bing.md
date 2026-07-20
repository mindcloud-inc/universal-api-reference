# ScrapingDog: Search Bing

Retrieves Bing search results through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-bing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-bing?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-bing?${params}`, {
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
| `query` | string | yes | Search query for Bing. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bing_data": {
        "displayed_link": "https://example.com",
        "images": [
          "string"
        ],
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
| `bing_data` | array<object> |  |
| `bing_data.displayed_link` | string |  |
| `bing_data.images` | array<string> |  |
| `bing_data.link` | string |  |
| `bing_data.rank` | number |  |
| `bing_data.snippet` | string |  |
| `bing_data.title` | string |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /bing/search` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-bing.md) for the provider-specific parameters and requirements.

