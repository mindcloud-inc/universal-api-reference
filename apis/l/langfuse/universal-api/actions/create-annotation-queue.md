# Langfuse: Create Annotation Queue

Creates an annotation queue in Langfuse.

```
POST https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/create-annotation-queue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langfuse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/create-annotation-queue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/create-annotation-queue', {
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
| `description` | string | no |  |
| `name` | string | no |  |
| `scoreConfigIds` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "scoreConfigIds": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `scoreConfigIds` | array<string> |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Langfuse API, this operation is `POST /annotation-queues` (base URL `https://cloud.langfuse.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-annotation-queue.md) for the provider-specific parameters and requirements.

