# Reoon Email Verifier: Verify Email Quick



```
GET https://connect.mindcloud.co/v1/universal/reoonEmailVerifier/latest/actions/verify-email-quick
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reoon Email Verifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reoonEmailVerifier/latest/actions/verify-email-quick?connectionId=$CONNECTION_ID&email=name%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "name@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reoonEmailVerifier/latest/actions/verify-email-quick?${params}`, {
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
| `email` | string | yes | The email address to verify in quick mode. Example: `name@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domain": "string",
      "email": "ava@example.com",
      "is_disposable": true,
      "is_free_email": true,
      "is_role_account": true,
      "is_spamtrap": true,
      "is_valid_syntax": true,
      "mx_accepts_mail": true,
      "mx_records": [
        "string"
      ],
      "status": "string",
      "username": "Ava Chen",
      "verification_mode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string |  |
| `email` | string |  |
| `is_disposable` | boolean |  |
| `is_free_email` | boolean |  |
| `is_role_account` | boolean |  |
| `is_spamtrap` | boolean |  |
| `is_valid_syntax` | boolean |  |
| `mx_accepts_mail` | boolean |  |
| `mx_records` | array<string> |  |
| `status` | string |  |
| `username` | string |  |
| `verification_mode` | string |  |

## Native endpoint

Through the native Reoon Email Verifier API, this operation is `GET /verify` (base URL `https://emailverifier.reoon.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email-quick.md) for the provider-specific parameters and requirements.

