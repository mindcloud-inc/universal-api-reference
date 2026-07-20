# QuickEmailVerification: Verify Email

Retrieves an email verification result from QuickEmailVerification.

```
GET https://connect.mindcloud.co/v1/universal/quickEmailVerification/latest/actions/verify-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickEmailVerification `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickEmailVerification/latest/actions/verify-email?connectionId=$CONNECTION_ID&email=richard%40quickemailverification.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "richard@quickemailverification.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickEmailVerification/latest/actions/verify-email?${params}`, {
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
| `email` | string | yes | Email address to verify. Example: `richard@quickemailverification.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accept_all": "string",
      "did_you_mean": "string",
      "disposable": "string",
      "domain": "string",
      "email": "ava@example.com",
      "free": "string",
      "message": "string",
      "mx_domain": "string",
      "mx_record": "string",
      "reason": "string",
      "result": "string",
      "role": "string",
      "safe_to_send": "string",
      "success": "string",
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accept_all` | string |  |
| `did_you_mean` | string |  |
| `disposable` | string |  |
| `domain` | string |  |
| `email` | string |  |
| `free` | string |  |
| `message` | string |  |
| `mx_domain` | string |  |
| `mx_record` | string |  |
| `reason` | string |  |
| `result` | string |  |
| `role` | string |  |
| `safe_to_send` | string |  |
| `success` | string |  |
| `user` | string |  |

## Native endpoint

Through the native QuickEmailVerification API, this operation is `GET /verify` (base URL `https://api.quickemailverification.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email.md) for the provider-specific parameters and requirements.

