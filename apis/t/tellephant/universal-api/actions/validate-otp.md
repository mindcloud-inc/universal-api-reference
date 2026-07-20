# Tellephant: Validate OTP

Validates an OTP code in Tellephant.

```
GET https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/validate-otp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tellephant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/validate-otp?connectionId=$CONNECTION_ID&otpId=string&otp=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "otpId": "string",
  "otp": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/validate-otp?${params}`, {
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
| `otpId` | string | yes | OTP ID returned by Send OTP. |
| `otp` | number | yes | One-time passcode entered by the user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": {},
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | object |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Tellephant API, this operation is `POST /v1/validate-otp` (base URL `https://api.tellephant.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-otp.md) for the provider-specific parameters and requirements.

