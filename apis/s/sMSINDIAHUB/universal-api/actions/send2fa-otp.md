# SMSINDIAHUB: Send 2FA OTP

Sends an auto-generated SMS OTP in SMSINDIAHUB.

```
POST https://connect.mindcloud.co/v1/universal/sMSINDIAHUB/latest/actions/send2fa-otp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSINDIAHUB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMSINDIAHUB/latest/actions/send2fa-otp" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSINDIAHUB/latest/actions/send2fa-otp', {
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



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SMSINDIAHUB API returns.

## Native endpoint

Through the native SMSINDIAHUB API, this operation is `GET /api1.php/v1/{apiKey}/sms/{contactNo}/{emailId}` (base URL `https://cloud.smsindiahub.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send2fa-otp.md) for the provider-specific parameters and requirements.

