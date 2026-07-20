# CINCEL: Request OTP



```
GET https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/request-otp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CINCEL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/request-otp?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/request-otp?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "host": "string",
      "isPro": true,
      "message": "string",
      "otpExpiresAt": "2026-05-07T12:00:00.000Z",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `host` | string | CINCEL host associated with the OTP request. |
| `isPro` | boolean | Whether the account is on a Pro tier. |
| `message` | string | Confirmation that the OTP was emailed. |
| `otpExpiresAt` | date | Timestamp when the OTP expires. |
| `statusCode` | number | HTTP-style status code returned by CINCEL. |

## Native endpoint

Through the native CINCEL API, this operation is `GET /tokens/otp` (base URL `https://api.cincel.digital/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-otp.md) for the provider-specific parameters and requirements.

