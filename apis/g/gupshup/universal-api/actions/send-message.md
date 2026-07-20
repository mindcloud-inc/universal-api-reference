# Gupshup: Send Message

Sends a WhatsApp message through Gupshup.

```
POST https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gupshup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "source": "string",
  "destination": "string",
  "message": {},
  "srcName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "source": "string",
    "destination": "string",
    "message": {},
    "srcName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `source` | string | yes | Registered WhatsApp Business API phone number. |
| `destination` | string | yes | User phone number to send the WhatsApp message to. |
| `message` | object | yes | Gupshup message object for the selected message type. |
| `srcName` | string | yes | Gupshup app name registered against the source phone number. |

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

Through the native Gupshup API, this operation is `POST /wa/api/v1/msg` (base URL `https://api.gupshup.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message.md) for the provider-specific parameters and requirements.

