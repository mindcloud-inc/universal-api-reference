# 2Chat: Send WhatsApp Message

Creates a WhatsApp message in 2Chat.

```
POST https://connect.mindcloud.co/v1/universal/chat/latest/actions/send-whats-app-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chat/latest/actions/send-whats-app-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fromNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chat/latest/actions/send-whats-app-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fromNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fromNumber` | string | yes | The WhatsApp number connected to 2Chat that sends the message. |
| `toNumber` | string | no | The WhatsApp phone number that receives the message. |
| `toGroupUuid` | string | no | The UUID of the WhatsApp group that receives the message. |
| `text` | string | no | The text content of the message. |
| `url` | string | no | A publicly accessible media file URL to attach. |
| `pin.latitude` | string | no | Latitude for an optional location pin. |
| `pin.longitude` | string | no | Longitude for an optional location pin. |
| `pin.name` | string | no | Name for an optional location pin. |
| `pin.address` | string | no | Address for an optional location pin. |
| `pin.url` | string | no | URL for an optional location pin. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batched": true,
      "messageUuid": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batched` | boolean |  |
| `messageUuid` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native 2Chat API, this operation is `POST /whatsapp/send-message` (base URL `https://api.p.2chat.io/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-whats-app-message.md) for the provider-specific parameters and requirements.

