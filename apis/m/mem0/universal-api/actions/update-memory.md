# Mem0: Update Memory

Updates an existing memory in Mem0.

```
PUT https://connect.mindcloud.co/v1/universal/mem0/latest/actions/update-memory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mem0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mem0/latest/actions/update-memory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "memory_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mem0/latest/actions/update-memory', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "memory_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `memory_id` | string | yes | Mem0 memory ID from the memory resource path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "memory": "string",
      "message": "string",
      "metadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `memory` | string |  |
| `message` | string |  |
| `metadata` | object |  |

## Native endpoint

Through the native Mem0 API, this operation is `PUT /v1/memories/:memory_id/` (base URL `https://api.mem0.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-memory.md) for the provider-specific parameters and requirements.

