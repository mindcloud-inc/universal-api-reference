# Tellephant: Send WhatsApp session message

Sends a WhatsApp session message through Tellephant.

```
POST https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/send-whats-app-session-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tellephant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/send-whats-app-session-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "to": 1,
  "whatsapp": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/send-whats-app-session-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "to": 1,
    "whatsapp": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `to` | number | yes | Recipient phone number with country code. |
| `whatsapp` | object | yes | WhatsApp session message payload object from Tellephant docs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": {},
      "message": "string",
      "messageId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | object |  |
| `message` | string |  |
| `messageId` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Tellephant API, this operation is `POST /v1/send-message` (base URL `https://api.tellephant.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-whats-app-session-message.md) for the provider-specific parameters and requirements.

