# LLMLayer: Search Web with Domain Filter

Searches the web in LLMLayer with domain filters.

```
GET https://connect.mindcloud.co/v1/universal/lLMLayer/latest/actions/search-web-with-domain-filter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LLMLayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lLMLayer/latest/actions/search-web-with-domain-filter?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lLMLayer/latest/actions/search-web-with-domain-filter?${params}`, {
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
| `domainFilter[]` | array<string> | no | Restrict results to one or more domains. |
| `query` | string | yes | Search query to run against the web. |

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

Through the native LLMLayer API, this operation is `POST /api/v2/web_search` (base URL `https://api.llmlayer.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-web-with-domain-filter.md) for the provider-specific parameters and requirements.

