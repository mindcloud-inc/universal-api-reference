# ChatDaddy: Update Chat

Updates an existing chat in ChatDaddy.

```
PUT https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/update-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatDaddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/update-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "acc_9d2c3b61-174e-42c5-be_0804",
  "action": "archive",
  "id": "sample-chat-id",
  "value": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/update-chat', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "acc_9d2c3b61-174e-42c5-be_0804",
    "action": "archive",
    "id": "sample-chat-id",
    "value": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | Account identifier for the chat. Default: `acc_9d2c3b61-174e-42c5-be_0804`. |
| `action` | string | yes | Chat action to perform, such as read, unread, archive, or pin. Default: `archive`. |
| `id` | string | yes | Chat identifier to update. Default: `sample-chat-id`. |
| `value` | string | yes | Value to apply for the selected chat action. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the chat update completed successfully. |

## Native endpoint

Through the native ChatDaddy API, this operation is `PATCH /chats/{accountId}/{id}` (base URL `https://api.chatdaddy.tech/im`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-chat.md) for the provider-specific parameters and requirements.

