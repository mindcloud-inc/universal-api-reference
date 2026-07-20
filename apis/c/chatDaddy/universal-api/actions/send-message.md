# ChatDaddy: Send Message

Sends a message to a ChatDaddy chat.

```
POST https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatDaddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "acc_9d2c3b61-174e-42c5-be_0804",
  "chatId": "sample-chat-id",
  "text": "Hello from ChatDaddy test"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "acc_9d2c3b61-174e-42c5-be_0804",
    "chatId": "sample-chat-id",
    "text": "Hello from ChatDaddy test"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | Account identifier to send from. Default: `acc_9d2c3b61-174e-42c5-be_0804`. |
| `chatId` | string | yes | Chat identifier to send the message to. Default: `sample-chat-id`. |
| `text` | string | yes | Message text content. Default: `Hello from ChatDaddy test`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Created message identifier. |
| `success` | boolean | Whether the message send request completed successfully. |

## Native endpoint

Through the native ChatDaddy API, this operation is `POST /messages/{accountId}/{chatId}` (base URL `https://api.chatdaddy.tech/im`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message.md) for the provider-specific parameters and requirements.

