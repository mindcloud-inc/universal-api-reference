# LabsMobile: Check OTP Code

Checks the status of an OTP code in LabsMobile.

```
GET https://connect.mindcloud.co/v1/universal/labsMobile/latest/actions/check-otp-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LabsMobile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/labsMobile/latest/actions/check-otp-code?connectionId=$CONNECTION_ID&phoneNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phoneNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/labsMobile/latest/actions/check-otp-code?${params}`, {
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
| `env` | string | no | OTP environment name. |
| `phoneNumber` | string | yes | Phone number to check. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LabsMobile API returns.

## Native endpoint

Through the native LabsMobile API, this operation is `GET /otp/checkCode` (base URL `https://api.labsmobile.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-otp-code.md) for the provider-specific parameters and requirements.

