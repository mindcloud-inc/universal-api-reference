# Agent Mail: List Inbox Messages

Retrieves messages from a specific AgentMail inbox.

```
GET https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/list-inbox-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent Mail `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/list-inbox-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&inboxId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "inboxId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/list-inbox-messages?${params}`, {
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
| `inboxId` | string | yes | The AgentMail inbox ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "from": "ava@example.com",
      "inbox_id": "string",
      "labels": [
        "string"
      ],
      "message_id": "string",
      "preview": "string",
      "size": 1,
      "subject": "string",
      "thread_id": "string",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "to": [
        "string"
      ],
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> | Message attachments. |
| `created_at` | date | Creation timestamp. |
| `from` | string | Sender address. |
| `inbox_id` | string | The ID of the inbox. |
| `labels` | array<string> | Labels on the message. |
| `message_id` | string | ID of the message. |
| `preview` | string | Message text preview. |
| `size` | number | Message size in bytes. |
| `subject` | string | Message subject. |
| `thread_id` | string | ID of the thread. |
| `timestamp` | date | Message sent or draft timestamp. |
| `to` | array<string> | Recipient addresses. |
| `updated_at` | date | Last update timestamp. |

## Native endpoint

Through the native Agent Mail API, this operation is `GET /inboxes/{inbox_id}/messages` (base URL `https://api.agentmail.to/v0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-inbox-messages.md) for the provider-specific parameters and requirements.

