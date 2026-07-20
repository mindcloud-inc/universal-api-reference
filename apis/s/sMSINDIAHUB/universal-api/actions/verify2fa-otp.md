# SMSINDIAHUB: Verify 2FA OTP

Retrieves SMS OTP verification results from SMSINDIAHUB.

```
GET https://connect.mindcloud.co/v1/universal/sMSINDIAHUB/latest/actions/verify2fa-otp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSINDIAHUB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSINDIAHUB/latest/actions/verify2fa-otp?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSINDIAHUB/latest/actions/verify2fa-otp?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SMSINDIAHUB API returns.

## Native endpoint

Through the native SMSINDIAHUB API, this operation is `GET /verify.php/API/V1/{apiKey}/SMS/VERIFY/{otpTokenId}/{otp}` (base URL `https://cloud.smsindiahub.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify2fa-otp.md) for the provider-specific parameters and requirements.

