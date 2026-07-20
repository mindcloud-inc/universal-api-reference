# Smart Sender: Assign Chat

Assigns a chat to an operator in Smart Sender.

```
PUT https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/assign-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smart Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/assign-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatId": "string",
  "operatorId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/assign-chat', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatId": "string",
    "operatorId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatId` | string | yes | The Smart Sender chat ID. |
| `operatorId` | string | yes | The Smart Sender operator ID that should receive the chat. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "state": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `state` | boolean |  |

## Native endpoint

Through the native Smart Sender API, this operation is `POST /v1/chats/:chatId/forward/:operatorId` (base URL `https://api.smartsender.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-chat.md) for the provider-specific parameters and requirements.

