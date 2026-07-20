# SMS Connexion: Cancel OTP

Deletes an existing OTP from SMS Connexion.

```
DELETE https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/cancel-otp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS Connexion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/cancel-otp?connectionId=$CONNECTION_ID&otpId=7e8c4d09-0ab2-4676-9d03-62460c3f92cc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "otpId": "7e8c4d09-0ab2-4676-9d03-62460c3f92cc"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/cancel-otp?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `otpId` | string | yes | OTP UUID returned by Create OTP. Example: `7e8c4d09-0ab2-4676-9d03-62460c3f92cc`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SMS Connexion API returns.

## Native endpoint

Through the native SMS Connexion API, this operation is `DELETE /otp/:otpId` (base URL `https://api.sms.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-otp.md) for the provider-specific parameters and requirements.

