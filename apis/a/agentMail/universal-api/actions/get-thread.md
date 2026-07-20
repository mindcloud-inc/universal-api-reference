# Agent Mail: Get Thread

Retrieves a specific thread from AgentMail.

```
GET https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/get-thread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/get-thread?connectionId=$CONNECTION_ID&threadId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "threadId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/get-thread?${params}`, {
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
| `threadId` | string | yes | The AgentMail thread ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "inbox_id": "string",
      "labels": [
        "string"
      ],
      "last_message_id": "string",
      "message_count": 1,
      "messages": [
        {}
      ],
      "preview": "string",
      "recipients": [
        "string"
      ],
      "senders": [
        "string"
      ],
      "size": 1,
      "subject": "string",
      "thread_id": "string",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Creation timestamp. |
| `inbox_id` | string | The ID of the inbox. |
| `labels` | array<string> | Labels on the thread. |
| `last_message_id` | string | ID of the last message in the thread. |
| `message_count` | number | Number of messages in the thread. |
| `messages` | array<object> | Messages in the thread. |
| `preview` | string | Preview of the last message. |
| `recipients` | array<string> | Thread recipient addresses. |
| `senders` | array<string> | Thread sender addresses. |
| `size` | number | Thread size in bytes. |
| `subject` | string | Thread subject. |
| `thread_id` | string | ID of the thread. |
| `timestamp` | date | Timestamp of the last sent or received message. |
| `updated_at` | date | Last update timestamp. |

## Native endpoint

Through the native Agent Mail API, this operation is `GET /threads/{thread_id}` (base URL `https://api.agentmail.to/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-thread.md) for the provider-specific parameters and requirements.

