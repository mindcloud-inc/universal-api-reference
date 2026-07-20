# LiveChat: Start Chat

Creates a new chat in LiveChat.

```
POST https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/start-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LiveChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/start-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chat.users[].id": "string",
  "chat.users[].type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/start-chat', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chat.users[].id": "string",
    "chat.users[].type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chat` | object | no | The chat payload to create. |
| `chat.properties` | object | no | Initial chat properties. |
| `chat.access` | object | no | Initial chat access settings. |
| `chat.users[]` | array<object> | no | Existing users to include in the chat. |
| `chat.users[].id` | string | yes | The user ID. |
| `chat.users[].type` | string | yes | Possible values: agent or customer. |
| `chat.thread` | object | no | The initial chat thread. |
| `chat.thread.events[]` | array<object> | no | Initial chat events. |
| `chat.thread.properties` | object | no | Initial thread properties. |
| `active` | boolean | no | Create an active thread by default. Default: `true`. |
| `continuous` | boolean | no | Start the chat in continuous mode. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chatId": "string",
      "eventIds": [
        "string"
      ],
      "threadId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chatId` | string | Identifier of the created chat. |
| `eventIds` | array<string> | Identifiers of user-generated initial events, when provided. |
| `threadId` | string | Identifier of the initial thread. |

## Native endpoint

Through the native LiveChat API, this operation is `POST /start_chat` (base URL `https://api.livechatinc.com/v3.6/agent/action`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-chat.md) for the provider-specific parameters and requirements.

