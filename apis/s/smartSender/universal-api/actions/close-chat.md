# Smart Sender: Close Chat

Closes a chat in Smart Sender.

```
PUT https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/close-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smart Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/close-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/close-chat', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatId` | string | yes | The Smart Sender chat ID. |

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

Through the native Smart Sender API, this operation is `PUT /v1/chats/:chatId/close` (base URL `https://api.smartsender.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/close-chat.md) for the provider-specific parameters and requirements.

