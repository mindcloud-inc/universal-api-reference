# Sozuri (Kenya) SMS: Send WhatsApp Sticker Message

Sends a WhatsApp sticker message through Sozuri.

```
POST https://connect.mindcloud.co/v1/universal/sozuriKenyaSMS/latest/actions/send-whats-app-sticker-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sozuri (Kenya) SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sozuriKenyaSMS/latest/actions/send-whats-app-sticker-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "string",
  "to": "string",
  "sticker": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sozuriKenyaSMS/latest/actions/send-whats-app-sticker-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "string",
    "to": "string",
    "sticker": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | yes | The WhatsApp business phone number or sender configured in your Sozuri project. |
| `campaign` | string | no | The campaign name for this message. |
| `to` | string | yes | The recipient phone number. |
| `sticker` | object | yes | The WhatsApp sticker payload object, including a publicly accessible link. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messageData": {},
      "recipients": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messageData` | object | The response metadata for the accepted WhatsApp send request. |
| `recipients` | array<object> | The list of recipients included in the request with acceptance status details. |

## Native endpoint

Through the native Sozuri (Kenya) SMS API, this operation is `POST /messaging` (base URL `https://sozuri.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-whats-app-sticker-message.md) for the provider-specific parameters and requirements.

