# MillionVerifier: Verify Email

Verifies an email address in MillionVerifier.

```
GET https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/verify-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MillionVerifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/verify-email?connectionId=$CONNECTION_ID&email=%5Bemail%C2%A0protected%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "[email protected]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/verify-email?${params}`, {
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
| `email` | string | yes | Email address to verify in real time. Example: `[email protected]`. |
| `timeout` | number | no | Time in seconds before the verification request times out. Default: `20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits": 1,
      "didyoumean": "string",
      "email": "ava@example.com",
      "error": "string",
      "executiontime": 1,
      "free": true,
      "livemode": true,
      "quality": "string",
      "result": "string",
      "resultcode": 1,
      "role": true,
      "subresult": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits` | number |  |
| `didyoumean` | string |  |
| `email` | string |  |
| `error` | string |  |
| `executiontime` | number |  |
| `free` | boolean |  |
| `livemode` | boolean |  |
| `quality` | string |  |
| `result` | string |  |
| `resultcode` | number |  |
| `role` | boolean |  |
| `subresult` | string |  |

## Native endpoint

Through the native MillionVerifier API, this operation is `GET /api/v3` (base URL `https://api.millionverifier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email.md) for the provider-specific parameters and requirements.

