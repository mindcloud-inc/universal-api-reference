# LiveChat: Send Rich Message Postback

Sends a rich message postback in LiveChat.

```
POST https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/send-rich-message-postback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LiveChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/send-rich-message-postback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatId": "string",
  "eventId": "string",
  "postback": {},
  "postback.id": "string",
  "postback.toggled": true,
  "threadId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/send-rich-message-postback', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatId": "string",
    "eventId": "string",
    "postback": {},
    "postback.id": "string",
    "postback.toggled": true,
    "threadId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatId` | string | yes | The chat ID. |
| `eventId` | string | yes | The rich message event ID. |
| `postback` | object | yes | The postback payload. |
| `postback.id` | string | yes | The postback name of the button. |
| `postback.toggled` | boolean | yes | Whether the postback is toggled. |
| `threadId` | string | yes | The thread ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Official Text Platform Agent Chat API docs specify this mutation returns no response payload (200 OK). |

## Native endpoint

Through the native LiveChat API, this operation is `POST /send_rich_message_postback` (base URL `https://api.livechatinc.com/v3.6/agent/action`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-rich-message-postback.md) for the provider-specific parameters and requirements.

