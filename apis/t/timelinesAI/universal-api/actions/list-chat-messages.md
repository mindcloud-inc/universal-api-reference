# TimelinesAI: List Chat Messages

Retrieves messages from a specific TimelinesAI chat.

```
GET https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/list-chat-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimelinesAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/list-chat-messages?connectionId=$CONNECTION_ID&chatId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/list-chat-messages?${params}`, {
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
| `chatId` | number | yes | ID of the chat in TimelinesAI. You can find it in the chat URL or outbound webhook payload. |
| `fromMe` | boolean | no | Filter messages sent from your WhatsApp account or received from others. |
| `after` | date | no | Filter messages created after this date or datetime. |
| `before` | date | no | Filter messages created before this date or datetime. |
| `afterMessage` | string | no | Filter messages created after the specified message UID. |
| `beforeMessage` | string | no | Filter messages created before the specified message UID. |
| `sortingOrder` | string | no | Order messages by timestamp using asc or desc. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "hasMorePages": true,
        "messages": [
          {
            "chatId": 1,
            "fromMe": true,
            "recipientName": "Ava Chen",
            "recipientPhone": "string",
            "senderName": "Ava Chen",
            "senderPhone": "string",
            "timestamp": "string",
            "uid": "string"
          }
        ]
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
| `data.hasMorePages` | boolean |  |
| `data.messages` | array<object> |  |
| `data.messages[].chatId` | number |  |
| `data.messages[].fromMe` | boolean |  |
| `data.messages[].recipientName` | string |  |
| `data.messages[].recipientPhone` | string |  |
| `data.messages[].senderName` | string |  |
| `data.messages[].senderPhone` | string |  |
| `data.messages[].timestamp` | string |  |
| `data.messages[].uid` | string |  |
| `status` | string |  |

## Native endpoint

Through the native TimelinesAI API, this operation is `GET /chats/{chat_id}/messages` (base URL `https://app.timelines.ai/integrations/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chat-messages.md) for the provider-specific parameters and requirements.

