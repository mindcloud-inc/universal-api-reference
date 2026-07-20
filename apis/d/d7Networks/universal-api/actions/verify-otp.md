# D7 Networks: Verify OTP

Verifies a one-time password with D7 Networks.

```
POST https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/verify-otp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a D7 Networks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/verify-otp" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "otp_id": "string",
  "otp_code": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/verify-otp', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "otp_id": "string",
    "otp_code": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `otp_id` | string | yes | OTP ID returned by Send OTP. |
| `otp_code` | string | yes | OTP code received by the recipient. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native D7 Networks API, this operation is `POST /verify/v1/otp/verify-otp` (base URL `https://api.d7networks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-otp.md) for the provider-specific parameters and requirements.

