# LEADTEX: Queue Text Message

Queues a text message by phone number in LEADTEX.

```
POST https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/queue-text-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LEADTEX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/queue-text-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phone": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/queue-text-message', {
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
| `phone` | string | yes | Recipient phone number when contact IDs are not supplied. |
| `text` | string | yes | Text message to queue. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact_id": 1,
      "errors": {},
      "message_id": "string",
      "phone": "string",
      "success": true,
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact_id` | number |  |
| `errors` | object |  |
| `message_id` | string |  |
| `phone` | string |  |
| `success` | boolean |  |
| `text` | string |  |

## Native endpoint

Through the native LEADTEX API, this operation is `POST /sendMessageToQueue?api_token={{credentials.apiKey}}` (base URL `https://app.leadteh.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/queue-text-message.md) for the provider-specific parameters and requirements.

