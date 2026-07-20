# Hunter: Verify Email



```
GET https://connect.mindcloud.co/v1/universal/hunter/latest/actions/verify-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hunter/latest/actions/verify-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hunter/latest/actions/verify-email?${params}`, {
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
| `email` | string | yes | Email address to verify. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptAll": true,
      "block": true,
      "disposable": true,
      "email": "ava@example.com",
      "gibberish": true,
      "mxRecords": true,
      "regexp": true,
      "result": "string",
      "score": 1,
      "smtpCheck": true,
      "smtpServer": true,
      "sources": [
        {}
      ],
      "status": "string",
      "webmail": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptAll` | boolean |  |
| `block` | boolean |  |
| `disposable` | boolean |  |
| `email` | string |  |
| `gibberish` | boolean |  |
| `mxRecords` | boolean |  |
| `regexp` | boolean |  |
| `result` | string |  |
| `score` | number |  |
| `smtpCheck` | boolean |  |
| `smtpServer` | boolean |  |
| `sources` | array<object> |  |
| `status` | string |  |
| `webmail` | boolean |  |

## Native endpoint

Through the native Hunter API, this operation is `GET /email-verifier` (base URL `https://api.hunter.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email.md) for the provider-specific parameters and requirements.

