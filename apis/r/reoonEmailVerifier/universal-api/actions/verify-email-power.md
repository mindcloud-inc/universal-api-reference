# Reoon Email Verifier: Verify Email Power



```
GET https://connect.mindcloud.co/v1/universal/reoonEmailVerifier/latest/actions/verify-email-power
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reoon Email Verifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reoonEmailVerifier/latest/actions/verify-email-power?connectionId=$CONNECTION_ID&email=name%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "name@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reoonEmailVerifier/latest/actions/verify-email-power?${params}`, {
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
| `email` | string | yes | The email address to verify in power mode. Example: `name@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "can_connect_smtp": true,
      "domain": "string",
      "email": "ava@example.com",
      "has_inbox_full": true,
      "is_catch_all": true,
      "is_deliverable": true,
      "is_disabled": true,
      "is_disposable": true,
      "is_free_email": true,
      "is_role_account": true,
      "is_safe_to_send": true,
      "is_spamtrap": true,
      "is_valid_syntax": true,
      "mx_accepts_mail": true,
      "mx_records": [
        "string"
      ],
      "overall_score": 1,
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
| `can_connect_smtp` | boolean |  |
| `domain` | string |  |
| `email` | string |  |
| `has_inbox_full` | boolean |  |
| `is_catch_all` | boolean |  |
| `is_deliverable` | boolean |  |
| `is_disabled` | boolean |  |
| `is_disposable` | boolean |  |
| `is_free_email` | boolean |  |
| `is_role_account` | boolean |  |
| `is_safe_to_send` | boolean |  |
| `is_spamtrap` | boolean |  |
| `is_valid_syntax` | boolean |  |
| `mx_accepts_mail` | boolean |  |
| `mx_records` | array<string> |  |
| `overall_score` | number |  |
| `status` | string |  |
| `username` | string |  |
| `verification_mode` | string |  |

## Native endpoint

Through the native Reoon Email Verifier API, this operation is `GET /verify` (base URL `https://emailverifier.reoon.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email-power.md) for the provider-specific parameters and requirements.

