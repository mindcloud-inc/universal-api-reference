# Seven: Send SMS

Creates a new SMS in Seven.

```
POST https://connect.mindcloud.co/v1/universal/seven/latest/actions/send-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seven/latest/actions/send-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "to": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seven/latest/actions/send-sms', {
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
| `to` | string | yes | Recipient number of the SMS. This can also be the name of a contact or a group. Our API accepts all common formats such as 0049171999999999 , 49171999999999 , +49171999999999 . Multiple recipients are transferred comma-separated. Ideally, you should enter the phone number in international format after E.164 . |
| `text` | string | yes | Text of the SMS message. |
| `from` | string | no | Sender of the SMS. This may contain a maximum of 11 alphanumeric or 16 numeric characters. |
| `delay` | date | no | Date/time for delayed sending. Optionally Unix timestamp or a timestamp in the format YYYY-MM-DD hh:mm:ss. |
| `flash` | boolean | no | Send SMS as Flash SMS. These are shown directly on the recipient&#x27;s display. On most devices, no sender is displayed for Flash SMS, with the exception of some older models. |
| `udh` | string | no | Individual User Data Header (UDH) of the SMS. If specified and variable text contains hex code, the message is sent as an 8-bit binary SMS. 050003CC0201 (concatenated message: reference number 204, part 1 of 2) |
| `ttl` | number | no | Specifies the validity period of the SMS in minutes. The default is 2880, i.e. 48 hours. Please note that not all networks allow a different setting. |
| `label` | string | no | Optionally set a separate label for each SMS so that you can assign it to your statistics. Max. 100 characters, permitted characters: a-z, A-Z, 0-9, .-_@. |
| `performanceTracking` | boolean | no | Activate click and performance tracking for URLs found in the SMS text. This also activates the URL shortener. |
| `foreignId` | string | no | Enter your own ID for this message. You will receive the foreign_id in turn for callbacks for status reports etc. Max. 64 characters, permitted characters: a-z, A-Z, 0-9, .-_@. |
| `isBinary` | boolean | no | If true , the SMS will be sent as binary data. |
| `getReplies` | boolean | no | Activates the reply function. Replies are assigned for 48 hours. The sender is automatically overwritten. |
| `unicode` | string | no |  |
| `utf8` | string | no |  |
| `returnMsgId` | string | no |  |
| `details` | string | no |  |
| `json` | string | no |  |
| `noReload` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": 1,
      "debug": "string",
      "messages": {
        "encoding": "string",
        "error": "string",
        "error_text": "string",
        "id": "string",
        "is_binary": true,
        "label": "string",
        "parts": 1,
        "price": 1,
        "recipient": "string",
        "sender": "string",
        "success": true,
        "text": "string",
        "udh": "string"
      },
      "sms_type": "string",
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
| `debug` | string |  |
| `messages` | array<object> |  |
| `messages.encoding` | string |  |
| `messages.error` | string |  |
| `messages.error_text` | string |  |
| `messages.id` | string |  |
| `messages.is_binary` | boolean |  |
| `messages.label` | string |  |
| `messages.parts` | number |  |
| `messages.price` | number |  |
| `messages.recipient` | string |  |
| `messages.sender` | string |  |
| `messages.success` | boolean |  |
| `messages.text` | string |  |
| `messages.udh` | string |  |
| `sms_type` | string |  |
| `success` | string |  |
| `total_price` | number |  |

## Native endpoint

Through the native Seven API, this operation is `POST /sms` (base URL `https://gateway.seven.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms.md) for the provider-specific parameters and requirements.

