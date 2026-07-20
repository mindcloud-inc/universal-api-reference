# ChatDaddy: Send Message to Chats

Sends a message to one or more ChatDaddy chats.

```
POST https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/send-message-to-chats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatDaddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/send-message-to-chats" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "acc_9d2c3b61-174e-42c5-be_0804",
  "recipients[]": [
    {
      "name": "Test Recipient",
      "phoneNumber": "15551239997"
    }
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/send-message-to-chats', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "acc_9d2c3b61-174e-42c5-be_0804",
    "recipients[]": [{"name":"Test Recipient","phoneNumber":"15551239997"}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | Account identifier to send from. Default: `acc_9d2c3b61-174e-42c5-be_0804`. |
| `compose` | object | no | Message composition payload, including text or attachments. |
| `recipients[]` | array<object> | yes | Recipient list for the bulk message send. Default: `[{"name":"Test Recipient","phoneNumber":"15551239997"}]`. |

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
| `success` | boolean | Whether the bulk message send request completed successfully. |

## Native endpoint

Through the native ChatDaddy API, this operation is `POST /messages` (base URL `https://api.chatdaddy.tech/im`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message-to-chats.md) for the provider-specific parameters and requirements.

