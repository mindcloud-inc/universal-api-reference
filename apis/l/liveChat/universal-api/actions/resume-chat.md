# LiveChat: Resume Chat

Restarts an archived chat in LiveChat.

```
POST https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/resume-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LiveChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/resume-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chat": {},
  "chat.id": "string",
  "chat.users[].id": "string",
  "chat.users[].type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/resume-chat', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chat": {},
    "chat.id": "string",
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
| `chat` | object | yes | The chat payload to resume. |
| `chat.id` | string | yes | The ID of the chat to resume. |
| `chat.access` | object | no | Chat access to set. |
| `chat.properties` | object | no | Initial chat properties. |
| `chat.users[]` | array<object> | no | Existing users to include in the resumed chat. |
| `chat.users[].id` | string | yes | The user ID. |
| `chat.users[].type` | string | yes | Possible values: agent or customer. |
| `chat.thread` | object | no | The initial resumed chat thread. |
| `chat.thread.events[]` | array<object> | no | Initial chat events. |
| `chat.thread.properties` | object | no | Initial thread properties. |
| `active` | boolean | no | Create an active thread by default. Default: `true`. |
| `continuous` | boolean | no | Leave chat continuous mode unchanged unless set. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `eventIds` | array<string> | Identifiers of user-generated initial events, when provided. |
| `threadId` | string | Identifier of the resumed thread. |

## Native endpoint

Through the native LiveChat API, this operation is `POST /resume_chat` (base URL `https://api.livechatinc.com/v3.6/agent/action`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resume-chat.md) for the provider-specific parameters and requirements.

