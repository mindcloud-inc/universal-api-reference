# Griptape: List Thread Messages

Finds messages in a Griptape thread.

```
GET https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-thread-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Griptape `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-thread-messages?connectionId=$CONNECTION_ID&threadId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "threadId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-thread-messages?${params}`, {
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
| `threadId` | string | yes | The Griptape thread ID whose messages should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messages": [
        {
          "created_at": "string",
          "created_by": "string",
          "index": 1,
          "input": "string",
          "message_id": "string",
          "metadata": {},
          "output": "string",
          "thread_id": "string",
          "updated_at": "string"
        }
      ],
      "pagination": {
        "page_number": 1,
        "page_size": 1,
        "total_count": 1,
        "total_pages": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messages[].created_at` | string |  |
| `messages[].created_by` | string |  |
| `messages[].index` | number |  |
| `messages[].input` | string |  |
| `messages[].message_id` | string |  |
| `messages[].metadata` | object |  |
| `messages[].output` | string |  |
| `messages[].thread_id` | string |  |
| `messages[].updated_at` | string |  |
| `pagination.page_number` | number |  |
| `pagination.page_size` | number |  |
| `pagination.total_count` | number |  |
| `pagination.total_pages` | number |  |

## Native endpoint

Through the native Griptape API, this operation is `GET /api/threads/:thread_id/messages` (base URL `https://cloud.griptape.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-thread-messages.md) for the provider-specific parameters and requirements.

