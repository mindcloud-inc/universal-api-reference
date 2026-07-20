# ChatDaddy: Update Message

Updates an existing message or note in ChatDaddy.

```
PUT https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/update-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatDaddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/update-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "acc_9d2c3b61-174e-42c5-be_0804",
  "chatId": "sample-chat-id",
  "id": "sample-message-id"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/update-message', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "acc_9d2c3b61-174e-42c5-be_0804",
    "chatId": "sample-chat-id",
    "id": "sample-message-id"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | Account identifier for the message. Default: `acc_9d2c3b61-174e-42c5-be_0804`. |
| `chatId` | string | yes | Chat identifier for the message. Default: `sample-chat-id`. |
| `id` | string | yes | Message identifier to update. Default: `sample-message-id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true,
      "updated": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the message update completed successfully. |
| `updated` | number | How many messages were updated. |

## Native endpoint

Through the native ChatDaddy API, this operation is `PATCH /messages/{accountId}/{chatId}/{id}` (base URL `https://api.chatdaddy.tech/im`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-message.md) for the provider-specific parameters and requirements.

