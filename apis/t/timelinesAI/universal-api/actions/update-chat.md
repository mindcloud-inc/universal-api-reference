# TimelinesAI: Update Chat

Updates an existing chat in TimelinesAI.

```
PUT https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/update-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimelinesAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/update-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/update-chat', {
  method: 'PUT',
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
| `name` | string | no | Unique chat name in the workspace. |
| `responsible` | string | no | Email address of the teammate to assign, or an empty string to unassign. |
| `closed` | boolean | no | Set the chat to closed or open. |
| `read` | boolean | no | Set the chat to read or unread. |
| `chatgptAutoresponseEnabled` | boolean | no | Enable or disable ChatGPT autoresponse for the chat. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "chatgptAutoresponseEnabled": true,
        "closed": true,
        "id": 1,
        "isGroup": true,
        "jid": "string",
        "labels": [
          "string"
        ],
        "name": "Ava Chen",
        "phone": "string",
        "read": true,
        "responsibleEmail": "ava@example.com"
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
| `data.chatgptAutoresponseEnabled` | boolean |  |
| `data.closed` | boolean |  |
| `data.id` | number |  |
| `data.isGroup` | boolean |  |
| `data.jid` | string |  |
| `data.labels` | array<string> |  |
| `data.name` | string |  |
| `data.phone` | string |  |
| `data.read` | boolean |  |
| `data.responsibleEmail` | string |  |
| `status` | string |  |

## Native endpoint

Through the native TimelinesAI API, this operation is `PATCH /chats/{chat_id}` (base URL `https://app.timelines.ai/integrations/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-chat.md) for the provider-specific parameters and requirements.

