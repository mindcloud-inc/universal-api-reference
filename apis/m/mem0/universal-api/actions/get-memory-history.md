# Mem0: Get Memory History

Retrieves a memory history from Mem0.

```
GET https://connect.mindcloud.co/v1/universal/mem0/latest/actions/get-memory-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mem0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mem0/latest/actions/get-memory-history?connectionId=$CONNECTION_ID&memory_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "memory_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mem0/latest/actions/get-memory-history?${params}`, {
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
| `memory_id` | string | yes | Mem0 memory ID from the memory resource path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "event": "string",
      "id": "string",
      "memory": "string",
      "metadata": {},
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
| `event` | string |  |
| `id` | string |  |
| `memory` | string |  |
| `metadata` | object |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Mem0 API, this operation is `GET /v1/memories/:memory_id/history/` (base URL `https://api.mem0.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-memory-history.md) for the provider-specific parameters and requirements.

