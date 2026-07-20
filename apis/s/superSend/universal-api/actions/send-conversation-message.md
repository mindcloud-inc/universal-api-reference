# SuperSend: Send Conversation Message

Creates a message in a SuperSend conversation.

```
POST https://connect.mindcloud.co/v1/universal/superSend/latest/actions/send-conversation-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/send-conversation-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superSend/latest/actions/send-conversation-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `message` | string | yes | Message content (required for all platforms) |
| `senderId` | string | no | Sender/mailbox ID to send from (required for email conversations). Must be an active sender in your organization. |
| `subject` | string | no | Email subject line (email only, defaults to "Re: {conversation title}") |
| `isHtml` | boolean | no | Whether the message is HTML formatted (email only) Default: false. |
| `to` | string | no | Override recipient email address (email only, auto-selected if not provided) |
| `cc[]` | array<string> | no | CC recipients (email only) |
| `bcc[]` | array<string> | no | BCC recipients (email only) |
| `attachments[]` | array<object> | no | Email attachments (email only) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {
          "cloud_url": "https://example.com",
          "file_path": "string",
          "filename": "Ava Chen",
          "id": "string"
        }
      ],
      "conversation_id": "string",
      "html": "string",
      "id": "string",
      "is_from_self": true,
      "is_read": true,
      "job_id": "string",
      "object": "string",
      "platform_type": "string",
      "sender": {
        "email": "ava@example.com",
        "id": "string"
      },
      "status": "string",
      "subject": "string",
      "text": "string",
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments[].cloud_url` | string |  |
| `attachments[].file_path` | string |  |
| `attachments[].filename` | string |  |
| `attachments[].id` | string |  |
| `conversation_id` | string |  |
| `html` | string |  |
| `id` | string |  |
| `is_from_self` | boolean |  |
| `is_read` | boolean |  |
| `job_id` | string |  |
| `object` | string |  |
| `platform_type` | string |  |
| `sender.email` | string |  |
| `sender.id` | string |  |
| `status` | string |  |
| `subject` | string |  |
| `text` | string |  |
| `timestamp` | date |  |

## Native endpoint

Through the native SuperSend API, this operation is `POST /conversations/{id}/messages` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-conversation-message.md) for the provider-specific parameters and requirements.

