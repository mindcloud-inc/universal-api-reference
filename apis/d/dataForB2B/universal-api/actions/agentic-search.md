# DataForB2B: Agentic Search

Searches DataForB2B with a prompt.

```
GET https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/agentic-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForB2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/agentic-search?connectionId=$CONNECTION_ID&query=Find%20software%20engineers%20at%20Google&category=people" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "Find software engineers at Google",
  "category": "people"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/agentic-search?${params}`, {
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
| `query` | string | yes | Natural-language query to run against DataForB2B. Default: `Find software engineers at Google`. |
| `category` | string | yes | Search category, such as people or company. Default: `people`. |
| `count` | number | no | Maximum number of results to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "query_interpretation": {},
      "results": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `query_interpretation` | object |  |
| `results` | array<object> |  |
| `total` | number |  |

## Native endpoint

Through the native DataForB2B API, this operation is `POST /search/llm` (base URL `https://api.dataforb2b.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/agentic-search.md) for the provider-specific parameters and requirements.

