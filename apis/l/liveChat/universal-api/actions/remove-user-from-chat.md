# LiveChat: Remove User From Chat

Updates a chat by removing a user in LiveChat.

```
PUT https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/remove-user-from-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LiveChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/remove-user-from-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatId": "string",
  "userId": "string",
  "userType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/remove-user-from-chat', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatId": "string",
    "userId": "string",
    "userType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatId` | string | yes | The target chat ID. |
| `userId` | string | yes | The user ID to remove. |
| `userType` | string | yes | Possible values: agent. |
| `ignoreRequesterPresence` | boolean | no | Allow the action even if the requester is not on the chat user list. Default: `false`. |

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

Through the native LiveChat API, this operation is `POST /remove_user_from_chat` (base URL `https://api.livechatinc.com/v3.6/agent/action`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-user-from-chat.md) for the provider-specific parameters and requirements.

