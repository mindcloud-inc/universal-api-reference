# WhatsBoost: Send OTP

Sends a one-time password from WhatsBoost.

```
POST https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/send-otp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsBoost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/send-otp" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "message": "string",
  "phone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/send-otp', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "message": "string",
    "phone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Type of message, it can be SMS or WhatsApp. |
| `message` | string | yes | OTP message to send, you can use {{otp}} shortcode to include the OTP anywhere in the message. |
| `phone` | string | yes | Recipient mobile number, it will accept E.164 formatted numbers. Example for Spain: E.164: +34612345678. |
| `expire` | number | no | OTP expiration time in seconds. Default value is 300 seconds or 5 minutes. |
| `priority` | number | no | For WhatsApp only. If you want to send the message as priority, it will be sent immediately. 1 for yes and 2 for no. |
| `account` | string | no | This is only for WhatsApp type. WhatsApp account you want to use for sending, you can get account unique IDs from /get/wa.accounts or in the dashboard. |
| `mode` | string | no | This is only required for SMS type. This is the mode of sending the message. 'devices' allows you to use linked Android devices, while 'credits' uses gateways and requires sufficient credit balance. |
| `device` | string | no | This is only for SMS type. Linked device unique ID, required for 'devices' mode. You can get linked device unique IDs from /get/devices (Your devices). |
| `gateway` | string | no | This is only for SMS type. Partner device unique ID or gateway ID, required for 'credits' mode. You can get partner device and gateway IDs from /get/rates. |
| `sim` | number | no | This is only for SMS type. SIM slot number you want to use, for 'devices' mode only. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native WhatsBoost API, this operation is `POST /send/otp` (base URL `https://whatsboost.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-otp.md) for the provider-specific parameters and requirements.

