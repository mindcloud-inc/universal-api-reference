# D7 Networks: Send OTP

Sends a one-time password with D7 Networks.

```
POST https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/send-otp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a D7 Networks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/send-otp" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recipient": "string",
  "content": "Your verification code is: {}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/send-otp', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recipient": "string",
    "content": "Your verification code is: {}"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recipient` | string | yes | Recipient phone number with country code. |
| `originator` | string | no | Sender ID or brand name. Default: `D7VERIFY`. |
| `content` | string | yes | OTP message content; include {} as the OTP placeholder. Default: `Your verification code is: {}`. |
| `expiry` | number | no | OTP expiry in seconds. Default: `600`. |
| `channel` | string | no | OTP delivery channel. Defaults to SMS. Default: `SMS`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data_coding` | string | no | Text encoding; text, unicode, or auto. Default: `text`. |

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

Through the native D7 Networks API, this operation is `POST /verify/v1/otp/send-otp` (base URL `https://api.d7networks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-otp.md) for the provider-specific parameters and requirements.

