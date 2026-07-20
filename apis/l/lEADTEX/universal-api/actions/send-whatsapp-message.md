# LEADTEX: Send WhatsApp Message

Sends a WhatsApp message by phone number in LEADTEX.

```
POST https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/send-whatsapp-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LEADTEX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/send-whatsapp-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phone": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/send-whatsapp-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phone": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phone` | string | yes | WhatsApp phone number. |
| `text` | string | yes | Message text to send. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "created_at": "2026-05-07T12:00:00.000Z",
        "id": 1,
        "messenger": "string",
        "name": "Ava Chen",
        "phone": "string"
      },
      "errors": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.created_at` | date |  |
| `data.id` | number |  |
| `data.messenger` | string |  |
| `data.name` | string |  |
| `data.phone` | string |  |
| `errors` | object |  |
| `message` | string |  |

## Native endpoint

Through the native LEADTEX API, this operation is `POST /sendMessageToWhatsApp?api_token={{credentials.apiKey}}` (base URL `https://app.leadteh.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-whatsapp-message.md) for the provider-specific parameters and requirements.

