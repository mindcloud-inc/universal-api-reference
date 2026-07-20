# Gupshup: Send Image Message

Sends an image WhatsApp message through Gupshup.

```
POST https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/send-image-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gupshup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/send-image-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/send-image-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channel` | string | no | Messaging channel. Gupshup WhatsApp send APIs use `whatsapp`. |
| `destination` | string | no | User phone number to send the WhatsApp message to. |
| `message` | string | no | Image message object, including image URLs and optional caption as documented by Gupshup. |
| `source` | string | no | Registered WhatsApp Business API phone number. |
| `srcName` | string | no | Gupshup app name registered against the source phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messageId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messageId` | string | Gupshup unique message identifier for the submitted message. |
| `status` | string | Submission status returned by Gupshup. |

## Native endpoint

Through the native Gupshup API, this operation is `POST /wa/api/v1/msg` (base URL `https://api.gupshup.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-image-message.md) for the provider-specific parameters and requirements.

