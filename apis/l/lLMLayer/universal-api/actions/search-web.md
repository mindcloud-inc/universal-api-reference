# LLMLayer: Search Web

Searches the web in LLMLayer for raw results.

```
GET https://connect.mindcloud.co/v1/universal/lLMLayer/latest/actions/search-web
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LLMLayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lLMLayer/latest/actions/search-web?connectionId=$CONNECTION_ID&query=Search%20query" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "Search query"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lLMLayer/latest/actions/search-web?${params}`, {
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
| `query` | string | yes | Search query to run against the web. Example: `Search query`. |
| `searchType` | string | no | Choose which LLMLayer search index to query. One of: `0`, `1`, `2`, `3`, `4`, `5`. Example: `Select search type`. |
| `location` | string | no | Optional location hint for localized results. Example: `us`. |
| `recency` | string | no | Optional recency filter for time-sensitive search types. One of: `0`, `1`, `2`, `3`, `4`. Example: `Select recency`. |
| `domainFilter` | string | no | Optional include/exclude domain list. Accepts multiple values as an array. Example: `example.com,-reddit.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cost": 1,
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cost` | number | Request cost charged by LLMLayer for this search. |
| `results` | array<object> | Raw LLMLayer search results returned for the query. |

## Native endpoint

Through the native LLMLayer API, this operation is `POST /api/v2/web_search` (base URL `https://api.llmlayer.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-web.md) for the provider-specific parameters and requirements.

