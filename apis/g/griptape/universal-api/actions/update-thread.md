# Griptape: Update Thread

Updates an existing thread in Griptape.

```
PUT https://connect.mindcloud.co/v1/universal/griptape/latest/actions/update-thread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Griptape `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/update-thread" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "threadId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/griptape/latest/actions/update-thread', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "threadId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `alias` | string | no | Optional new alias for the thread. |
| `name` | string | no | Optional new thread name. |
| `threadId` | string | yes | The Griptape thread ID to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "created_at": "string",
      "created_by": "string",
      "message_count": 1,
      "messages_length": 1,
      "metadata": {},
      "name": "Ava Chen",
      "organization_id": "string",
      "thread_id": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `created_at` | string |  |
| `created_by` | string |  |
| `message_count` | number |  |
| `messages_length` | number |  |
| `metadata` | object |  |
| `name` | string |  |
| `organization_id` | string |  |
| `thread_id` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Griptape API, this operation is `PATCH /api/threads/:thread_id` (base URL `https://cloud.griptape.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-thread.md) for the provider-specific parameters and requirements.

