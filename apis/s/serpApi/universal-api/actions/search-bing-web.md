# SerpApi: Search Bing Web

Retrieves Bing web search results from SerpApi.

```
GET https://connect.mindcloud.co/v1/universal/serpApi/latest/actions/search-bing-web
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SerpApi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serpApi/latest/actions/search-bing-web?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serpApi/latest/actions/search-bing-web?${params}`, {
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
| `q` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayed_link": "https://example.com",
      "link": "https://example.com",
      "snippet": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayed_link` | string |  |
| `link` | string |  |
| `snippet` | string |  |
| `title` | string |  |

## Native endpoint

Through the native SerpApi API, this operation is `GET /search.json` (base URL `https://serpapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-bing-web.md) for the provider-specific parameters and requirements.

