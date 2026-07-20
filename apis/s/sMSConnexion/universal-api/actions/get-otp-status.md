# SMS Connexion: Get OTP Status

Retrieves an OTP status from SMS Connexion.

```
GET https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-otp-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS Connexion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-otp-status?connectionId=$CONNECTION_ID&otpId=7e8c4d09-0ab2-4676-9d03-62460c3f92cc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "otpId": "7e8c4d09-0ab2-4676-9d03-62460c3f92cc"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-otp-status?${params}`, {
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

```json
{
  "success": true,
  "data": [
    {
      "attempts": 1,
      "cost": 1,
      "countryIso": "string",
      "dateCreated": "string",
      "dateExpires": "string",
      "maxAttempts": 1,
      "otpId": "string",
      "parts": 1,
      "phoneNumber": "string",
      "status": "string",
      "trackId": "string",
      "ttl": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attempts` | number |  |
| `cost` | number |  |
| `countryIso` | string |  |
| `dateCreated` | string |  |
| `dateExpires` | string |  |
| `maxAttempts` | number |  |
| `otpId` | string |  |
| `parts` | number |  |
| `phoneNumber` | string |  |
| `status` | string |  |
| `trackId` | string |  |
| `ttl` | number |  |

## Native endpoint

Through the native SMS Connexion API, this operation is `GET /otp/:otpId` (base URL `https://api.sms.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-otp-status.md) for the provider-specific parameters and requirements.

