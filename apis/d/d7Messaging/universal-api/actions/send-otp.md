# D7 Messaging: Send OTP

Sends a one-time password through D7 Messaging.

```
POST https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/send-otp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a D7 Messaging `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/send-otp" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recipient": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/send-otp', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recipient": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recipient` | string | yes | Recipient phone number in E.164 format including country code. |
| `content` | string | no | OTP message content. Use {} where the OTP code should be inserted. |
| `templateId` | number | no | Dashboard template ID to use instead of Content. |
| `originator` | string | no | Sender name shown to the recipient. Default: `D7VERIFY`. |
| `channel` | string | no | Channel used to deliver the OTP, such as SMS or WhatsApp. Default: `SMS`. |
| `expiry` | number | no | OTP validity period in seconds. Default: `600`. |
| `dataCoding` | string | no | Encoding mode for the OTP content: text, unicode, or auto. Default: `text`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expiry": 1,
      "otp_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiry` | number |  |
| `otp_id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native D7 Messaging API, this operation is `POST /verify/v1/otp/send-otp` (base URL `https://api.d7networks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-otp.md) for the provider-specific parameters and requirements.

