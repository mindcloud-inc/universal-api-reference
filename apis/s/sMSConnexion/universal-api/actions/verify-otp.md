# SMS Connexion: Verify OTP

Verifies an OTP in SMS Connexion.

```
PUT https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/verify-otp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS Connexion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/verify-otp" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "otpId": "7e8c4d09-0ab2-4676-9d03-62460c3f92cc",
  "pin": "123456"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/verify-otp', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "otpId": "7e8c4d09-0ab2-4676-9d03-62460c3f92cc",
    "pin": "123456"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `otpId` | string | yes | OTP UUID returned by Create OTP. Example: `7e8c4d09-0ab2-4676-9d03-62460c3f92cc`. |
| `pin` | string | yes | OTP PIN code to verify. Example: `123456`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native SMS Connexion API, this operation is `POST /otp/:otpId` (base URL `https://api.sms.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-otp.md) for the provider-specific parameters and requirements.

