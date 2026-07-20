# Usedesk: Change Chat Assignee

Updates a chat assignee in Usedesk.

```
PUT https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/change-chat-assignee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Usedesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/change-chat-assignee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatId": 1,
  "userId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/change-chat-assignee', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatId": 1,
    "userId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatId` | number | yes | Chat ID. |
| `userId` | number | yes | ID of the agent you want to assign the chat to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chat_id": 1,
      "url": "https://example.com",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chat_id` | number |  |
| `url` | string |  |
| `user_id` | number |  |

## Native endpoint

Through the native Usedesk API, this operation is `POST /chat/changeAssignee` (base URL `https://secure.usedesk.com/uapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-chat-assignee.md) for the provider-specific parameters and requirements.

