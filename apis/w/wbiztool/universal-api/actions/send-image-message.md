# Wbiztool: Send Image Message

Creates a WhatsApp image message in Wbiztool.

```
POST https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/send-image-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wbiztool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/send-image-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageUrl": "https://example.com",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/send-image-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageUrl": "https://example.com",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phone` | string | no | Recipient phone number with or without country code. |
| `groupName` | string | no | WhatsApp group name to message instead of a direct phone number. |
| `countryCode` | string | no | Country code for the recipient phone number. |
| `imageUrl` | string | yes | Public image URL to include with the message. |
| `message` | string | yes | Caption text to send with the image. |
| `webhookUrl` | string | no | Optional webhook URL to receive message events. |
| `expireAfterSeconds` | number | no | Expire the message if it has not been sent before this many seconds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "msgId": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `msgId` | number |  |
| `status` | number |  |

## Native endpoint

Through the native Wbiztool API, this operation is `POST /send_msg/` (base URL `https://wbiztool.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-image-message.md) for the provider-specific parameters and requirements.

