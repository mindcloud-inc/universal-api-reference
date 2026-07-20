# Open AI: List Vector Stores

Retrieves vector stores from Open AI.

```
GET https://connect.mindcloud.co/v1/universal/openAi/latest/actions/list-vector-stores
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/list-vector-stores?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openAi/latest/actions/list-vector-stores?${params}`, {
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
| `limit` | number | no | Maximum number of vector stores to return. Default: `20`. |
| `order` | string | no | Sort order by created time. Default: `desc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "created_at": 1,
          "id": "string",
          "name": "Ava Chen",
          "object": "string",
          "status": "string",
          "usage_bytes": 1
        }
      ],
      "has_more": true,
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Returned vector stores. |
| `data[].created_at` | number | Creation timestamp. |
| `data[].id` | string | Vector store ID. |
| `data[].name` | string | Vector store name. |
| `data[].object` | string | Object type. |
| `data[].status` | string | Vector store status. |
| `data[].usage_bytes` | number | Storage usage in bytes. |
| `has_more` | boolean | Whether more vector stores are available. |
| `object` | string | List object type. |

## Native endpoint

Through the native Open AI API, this operation is `GET v1/vector_stores` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vector-stores.md) for the provider-specific parameters and requirements.

