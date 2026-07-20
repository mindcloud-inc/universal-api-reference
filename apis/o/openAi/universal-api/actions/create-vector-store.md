# Open AI: Create Vector Store

Creates a vector store in Open AI.

```
POST https://connect.mindcloud.co/v1/universal/openAi/latest/actions/create-vector-store
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/create-vector-store" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openAi/latest/actions/create-vector-store', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Optional name for the vector store. |
| `file_ids[]` | array<string> | no | Optional file IDs to attach at creation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": {},
      "expiresAfter": {},
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "fileCounts": {
        "cancelled": 1,
        "completed": 1,
        "failed": 1,
        "inProgress": 1,
        "total": 1
      },
      "id": "string",
      "lastActiveAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "object": "string",
      "status": "string",
      "usageBytes": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `description` | object |  |
| `expiresAfter` | object |  |
| `expiresAt` | date |  |
| `fileCounts.cancelled` | number |  |
| `fileCounts.completed` | number |  |
| `fileCounts.failed` | number |  |
| `fileCounts.inProgress` | number |  |
| `fileCounts.total` | number |  |
| `id` | string |  |
| `lastActiveAt` | date |  |
| `name` | string |  |
| `object` | string |  |
| `status` | string |  |
| `usageBytes` | number |  |

## Native endpoint

Through the native Open AI API, this operation is `POST v1/vector_stores` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vector-store.md) for the provider-specific parameters and requirements.

