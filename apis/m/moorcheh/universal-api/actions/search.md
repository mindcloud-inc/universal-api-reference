# Moorcheh: Search

Finds relevant results in Moorcheh across selected namespaces.

```
GET https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moorcheh `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/search?connectionId=$CONNECTION_ID&query=string&namespaces%5B%5D=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string",
  "namespaces[]": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/search?${params}`, {
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
| `query` | string | yes | Search query text. Metadata and keyword filters can be placed at the end of the query using Moorcheh syntax. |
| `namespaces[]` | array<string> | yes | Array of namespace names to search. All namespaces must be of the same type. |
| `top_k` | number | no | Number of top relevant chunks to return. Defaults to 10 in Moorcheh. Default: `10`. |
| `kiosk_mode` | boolean | no | When enabled, Moorcheh filters chunks below the threshold. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `threshold` | number | no | Minimum relevance score from 0 to 1. Required by Moorcheh when kiosk mode is enabled. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "execution_time": 1,
      "optimization_info": {},
      "results": [
        {
          "id": "string",
          "label": "string",
          "metadata": {},
          "score": 1,
          "text": "string"
        }
      ],
      "timings": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `execution_time` | number | Total execution time in seconds. |
| `optimization_info` | object | Search optimization details. |
| `results` | array<object> | Search results ordered by relevance. |
| `results[].id` | string | Document or vector identifier. |
| `results[].label` | string | Human-readable relevance label. |
| `results[].metadata` | object | Additional metadata associated with the result. |
| `results[].score` | number | ITS relevance score. |
| `results[].text` | string | Original text for text namespaces. |
| `timings` | object | Detailed timing breakdown. |

## Native endpoint

Through the native Moorcheh API, this operation is `POST /search` (base URL `https://api.moorcheh.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search.md) for the provider-specific parameters and requirements.

