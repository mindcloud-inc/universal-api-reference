# SMS Connexion: Create OTP

Creates a new OTP in SMS Connexion.

```
POST https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/create-otp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS Connexion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/create-otp" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phoneNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/create-otp', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phoneNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phoneNumber` | string | yes | Recipient phone number in E.164 format. |

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
      "otpCallbackUrl": "https://example.com",
      "otpId": "string",
      "parts": 1,
      "phoneNumber": "string",
      "status": "string",
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
| `otpCallbackUrl` | string |  |
| `otpId` | string |  |
| `parts` | number |  |
| `phoneNumber` | string |  |
| `status` | string |  |
| `ttl` | number |  |

## Native endpoint

Through the native SMS Connexion API, this operation is `POST /otp` (base URL `https://api.sms.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-otp.md) for the provider-specific parameters and requirements.

