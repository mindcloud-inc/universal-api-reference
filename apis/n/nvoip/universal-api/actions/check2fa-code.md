# Nvoip: Check 2FA Code



```
GET https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/check2fa-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nvoip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/check2fa-code?connectionId=$CONNECTION_ID&pin=string&token2fa=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pin": "string",
  "token2fa": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/check2fa-code?${params}`, {
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
| `pin` | string | yes | Verification PIN received by the user. |
| `token2fa` | string | yes | Token returned by the Send 2FA Code action. |

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
| `status` | string | Validation status returned by Nvoip when the 2FA code is checked. |

## Native endpoint

Through the native Nvoip API, this operation is `GET /check/2fa` (base URL `https://api.nvoip.com.br/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check2fa-code.md) for the provider-specific parameters and requirements.

