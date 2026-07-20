# Nvoip: Check OTP



```
GET https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/check-otp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nvoip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/check-otp?connectionId=$CONNECTION_ID&code=string&key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "code": "string",
  "key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/check-otp?${params}`, {
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
| `code` | string | yes | OTP code received by the user. |
| `key` | string | yes | OTP key returned by the Send OTP action. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider error or validation message returned by Nvoip. |
| `status` | string | Validation status returned by Nvoip when the OTP code is checked. |

## Native endpoint

Through the native Nvoip API, this operation is `GET /check/otp` (base URL `https://api.nvoip.com.br/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-otp.md) for the provider-specific parameters and requirements.

