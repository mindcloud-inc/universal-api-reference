# CINCEL: Exchange OTP For JWT



```
GET https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/exchange-otp-for-jwt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CINCEL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/exchange-otp-for-jwt?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/exchange-otp-for-jwt?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CINCEL API returns.

## Native endpoint

Through the native CINCEL API, this operation is `GET /tokens/jwt` (base URL `https://api.cincel.digital/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/exchange-otp-for-jwt.md) for the provider-specific parameters and requirements.

