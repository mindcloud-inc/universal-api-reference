# Agent Mail: Get Inbox Message

Retrieves a message from a specific AgentMail inbox.

```
GET https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/get-inbox-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/get-inbox-message?connectionId=$CONNECTION_ID&inboxId=string&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inboxId": "string",
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/get-inbox-message?${params}`, {
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
| `messageId` | string | yes | The AgentMail message ID. |

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
      "html": "string",
      "inbox_id": "string",
      "labels": [
        "string"
      ],
      "message_id": "string",
      "preview": "string",
      "size": 1,
      "subject": "string",
      "text": "string",
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
| `html` | string | HTML body. |
| `inbox_id` | string | The ID of the inbox. |
| `labels` | array<string> | Labels on the message. |
| `message_id` | string | ID of the message. |
| `preview` | string | Message text preview. |
| `size` | number | Message size in bytes. |
| `subject` | string | Message subject. |
| `text` | string | Plain text body. |
| `thread_id` | string | ID of the thread. |
| `timestamp` | date | Message sent or draft timestamp. |
| `to` | array<string> | Recipient addresses. |
| `updated_at` | date | Last update timestamp. |

## Native endpoint

Through the native Agent Mail API, this operation is `GET /inboxes/{inbox_id}/messages/{message_id}` (base URL `https://api.agentmail.to/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inbox-message.md) for the provider-specific parameters and requirements.

