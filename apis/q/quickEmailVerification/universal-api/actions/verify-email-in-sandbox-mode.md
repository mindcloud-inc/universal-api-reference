# QuickEmailVerification: Verify Email in Sandbox Mode

Retrieves a simulated email verification result from QuickEmailVerification.

```
GET https://connect.mindcloud.co/v1/universal/quickEmailVerification/latest/actions/verify-email-in-sandbox-mode
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickEmailVerification `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickEmailVerification/latest/actions/verify-email-in-sandbox-mode?connectionId=$CONNECTION_ID&email=safe-to-send%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "safe-to-send@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickEmailVerification/latest/actions/verify-email-in-sandbox-mode?${params}`, {
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
| `email` | string | yes | Email address to test against QuickEmailVerification sandbox responses. Example: `safe-to-send@example.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allowedIp` | boolean | no | Optional sandbox flag to simulate IP allowlist failures. Example: `false`. |

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
| `reason` | string |  |
| `result` | string |  |
| `role` | string |  |
| `safe_to_send` | string |  |
| `success` | string |  |
| `user` | string |  |

## Native endpoint

Through the native QuickEmailVerification API, this operation is `GET /verify/sandbox` (base URL `https://api.quickemailverification.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email-in-sandbox-mode.md) for the provider-specific parameters and requirements.

