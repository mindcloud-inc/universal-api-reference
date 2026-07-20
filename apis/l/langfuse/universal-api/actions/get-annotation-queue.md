# Langfuse: Get Annotation Queue

Retrieves an annotation queue from Langfuse.

```
GET https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/get-annotation-queue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langfuse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/get-annotation-queue?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/get-annotation-queue?${params}`, {
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
| `queueId` | string | no |  |

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

Through the native Langfuse API, this operation is `GET /annotation-queues/:queueId` (base URL `https://cloud.langfuse.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-annotation-queue.md) for the provider-specific parameters and requirements.

