# Nvoip: Send OTP



```
POST https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/send-otp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nvoip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/send-otp" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/send-otp', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | Email address that should receive the OTP. |
| `sms` | string | no | Phone number that should receive the OTP by SMS. |
| `voice` | string | no | Phone number that should receive the OTP by voice. |
| `methods.email` | boolean | no | Whether to deliver the OTP by email. Default: `false`. |
| `methods.sms` | boolean | no | Whether to deliver the OTP by SMS. Default: `false`. |
| `methods.voice` | boolean | no | Whether to deliver the OTP by voice call. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expiresIn": "string",
      "key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiresIn` | string | Expiration timestamp for the OTP key. |
| `key` | string | Provider key used to validate the OTP. |

## Native endpoint

Through the native Nvoip API, this operation is `POST /otp` (base URL `https://api.nvoip.com.br/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-otp.md) for the provider-specific parameters and requirements.

