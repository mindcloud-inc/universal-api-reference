# Seven: Send Voice Call

Creates a new voice call in Seven.

```
POST https://connect.mindcloud.co/v1/universal/seven/latest/actions/send-voice-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seven/latest/actions/send-voice-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "to": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seven/latest/actions/send-voice-call', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "to": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `to` | string | yes | Recipient number(s) of the voice calls. This can also be the name of a contact or a group. Our API accepts all common formats like 0049171123456789 , 49171123456789 , +49171123456789 . Multiple recipients are passed separated by commas. Ideally, you should provide the phone number in the international format according to E.164 . |
| `text` | string | yes | Text message to be read out. Optionally as simple text or as SSML . |
| `from` | string | no | Caller ID of the call. Please only use verified sender IDs or one of your numbers booked with us here. |
| `ringtime` | number | no | The duration of how long it should ring at the recipient&#x27;s end before hanging up. Here, 5 to 60 seconds are possible. |
| `foreignId` | string | no | A unique ID that you can use for later assignment of the call. This ID is passed in the webhook events. |
| `xml` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": 1,
      "debug": true,
      "messages": {
        "error": "string",
        "error_text": "string",
        "id": 1,
        "price": 1,
        "recipient": "string",
        "sender": "string",
        "success": true,
        "text": "string"
      },
      "success": "string",
      "total_price": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number |  |
| `debug` | boolean |  |
| `messages` | array<object> |  |
| `messages.error` | string |  |
| `messages.error_text` | string |  |
| `messages.id` | number |  |
| `messages.price` | number |  |
| `messages.recipient` | string |  |
| `messages.sender` | string |  |
| `messages.success` | boolean |  |
| `messages.text` | string |  |
| `success` | string |  |
| `total_price` | number |  |

## Native endpoint

Through the native Seven API, this operation is `POST /voice` (base URL `https://gateway.seven.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-voice-call.md) for the provider-specific parameters and requirements.

