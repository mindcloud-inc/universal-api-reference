# Mocean API: Check Verify Code



```
GET https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/check-verify-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mocean API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/check-verify-code?connectionId=$CONNECTION_ID&code=string&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "code": "string",
  "requestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/check-verify-code?${params}`, {
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
| `code` | string | yes | Verification code to check. |
| `requestId` | string | yes | Verify request ID returned by Mocean. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "requestId": "string",
      "status": 1,
      "valid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string |  |
| `requestId` | string |  |
| `status` | number |  |
| `valid` | boolean |  |

## Native endpoint

Through the native Mocean API API, this operation is `POST /rest/2/verify/check?mocean-resp-format=json` (base URL `https://rest.moceanapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-verify-code.md) for the provider-specific parameters and requirements.

