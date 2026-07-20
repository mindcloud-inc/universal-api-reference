# Griptape: Get Thread

Retrieves a thread from Griptape.

```
GET https://connect.mindcloud.co/v1/universal/griptape/latest/actions/get-thread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Griptape `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/get-thread?connectionId=$CONNECTION_ID&threadId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "threadId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/griptape/latest/actions/get-thread?${params}`, {
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
| `threadId` | string | yes | The Griptape thread ID to retrieve. |

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

Through the native Griptape API, this operation is `GET /api/threads/:thread_id` (base URL `https://cloud.griptape.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-thread.md) for the provider-specific parameters and requirements.

