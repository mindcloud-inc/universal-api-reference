# Authkey: Verify 2FA OTP

Verifies a 2FA OTP in Authkey.

```
POST https://connect.mindcloud.co/v1/universal/authkey/latest/actions/verify2fa-otp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Authkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/authkey/latest/actions/verify2fa-otp" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channel": "SMS",
  "otp": "123456",
  "logId": "28bf7375bb54540ba03a4eb873d4da44"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/authkey/latest/actions/verify2fa-otp', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channel": "SMS",
    "otp": "123456",
    "logId": "28bf7375bb54540ba03a4eb873d4da44"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channel` | string | yes | Verification channel: SMS, VOICE, or EMAIL. Example: `SMS`. |
| `otp` | string | yes | OTP code entered by the customer. Example: `123456`. |
| `logId` | string | yes | Log ID returned by the Start 2FA Session action. Example: `28bf7375bb54540ba03a4eb873d4da44`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Authkey API returns.

## Native endpoint

Through the native Authkey API, this operation is `GET https://console.authkey.io/api/2fa_verify.php` (base URL `https://console.authkey.io/restapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify2fa-otp.md) for the provider-specific parameters and requirements.

