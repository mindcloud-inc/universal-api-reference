# Mem0: List Memories



```
GET https://connect.mindcloud.co/v1/universal/mem0/latest/actions/list-memories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mem0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mem0/latest/actions/list-memories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mem0/latest/actions/list-memories?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "expiration_date": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "immutable": true,
      "memory": "string",
      "metadata": {},
      "organization": "string",
      "owner": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `expiration_date` | date |  |
| `id` | string |  |
| `immutable` | boolean |  |
| `memory` | string |  |
| `metadata` | object |  |
| `organization` | string |  |
| `owner` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Mem0 API, this operation is `POST /v2/memories/` (base URL `https://api.mem0.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-memories.md) for the provider-specific parameters and requirements.

