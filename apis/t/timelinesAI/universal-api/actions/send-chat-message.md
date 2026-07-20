# TimelinesAI: Send Chat Message

Creates a new message in an existing TimelinesAI chat.

```
POST https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/send-chat-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimelinesAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/send-chat-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/send-chat-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatId` | number | yes | ID of the chat in TimelinesAI. You can find it in the chat URL or outbound webhook payload. |
| `text` | string | no | Plain text message to send. |
| `fileUid` | string | no | Uploaded attachment UID to send with the message. |
| `label` | string | no | Label to assign to the chat while sending the message. |
| `attachmentTemplateId` | number | no | Attachment template ID to send with the message. |
| `replyTo` | string | no | Message UID to reply to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "messageUid": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.messageUid` | string |  |
| `status` | string |  |

## Native endpoint

Through the native TimelinesAI API, this operation is `POST /chats/{chat_id}/messages` (base URL `https://app.timelines.ai/integrations/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-chat-message.md) for the provider-specific parameters and requirements.

