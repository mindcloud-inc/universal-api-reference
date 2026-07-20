# D7 Messaging: Resend OTP

Resends a one-time password through D7 Messaging.

```
POST https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/resend-otp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a D7 Messaging `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/resend-otp" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "otpId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/resend-otp', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "otpId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `otpId` | string | yes | OTP ID returned by Send OTP. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expiry": 1,
      "otp_id": "string",
      "resend_count": 1,
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
| `resend_count` | number |  |
| `status` | string |  |

## Native endpoint

Through the native D7 Messaging API, this operation is `POST /verify/v1/otp/resend-otp` (base URL `https://api.d7networks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resend-otp.md) for the provider-specific parameters and requirements.

