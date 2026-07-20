# Open AI: Update Vector Store

Updates a vector store in Open AI.

```
PUT https://connect.mindcloud.co/v1/universal/openAi/latest/actions/update-vector-store
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/update-vector-store" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloud Runtime Store Renamed",
  "vector_store_id": "vs_69d92e3185648191aa8ab6d69a154540"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openAi/latest/actions/update-vector-store', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloud Runtime Store Renamed",
    "vector_store_id": "vs_69d92e3185648191aa8ab6d69a154540"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Updated vector store name. Default: `MindCloud Runtime Store Renamed`. |
| `vector_store_id` | string | yes | Vector store ID to update. Default: `vs_69d92e3185648191aa8ab6d69a154540`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": 1,
      "description": "string",
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "object": "string",
      "status": "string",
      "usage_bytes": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | number | Creation timestamp. |
| `description` | string | Vector store description. |
| `id` | string | Vector store ID. |
| `metadata` | object | Attached metadata. |
| `name` | string | Vector store name. |
| `object` | string | Object type. |
| `status` | string | Vector store status. |
| `usage_bytes` | number | Storage usage in bytes. |

## Native endpoint

Through the native Open AI API, this operation is `POST v1/vector_stores/:vector_store_id` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-vector-store.md) for the provider-specific parameters and requirements.

