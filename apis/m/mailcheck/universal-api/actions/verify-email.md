# Mailcheck: Verify Email



```
POST https://connect.mindcloud.co/v1/universal/mailcheck/latest/actions/verify-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailcheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailcheck/latest/actions/verify-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "user@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailcheck/latest/actions/verify-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "user@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address to verify. Example: `user@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cached": true,
      "checks": {
        "disposable": "string",
        "free_provider": true,
        "mx": "string",
        "role": "string",
        "smtp": "string",
        "syntax": "string"
      },
      "credits_remaining": 1,
      "details": {
        "catch_all": true,
        "catchAll": true,
        "has_typo_suggestion": true,
        "is_disposable": true,
        "is_free_provider": true,
        "is_role": true,
        "mxHost": "string",
        "risk_level": "string"
      },
      "email": "ava@example.com",
      "reason": "string",
      "score": 1,
      "valid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cached` | boolean | Whether the result came from cache. |
| `checks` | object | Per-check outcomes. |
| `checks.disposable` | string | Disposable-email check result. |
| `checks.free_provider` | boolean | Whether the provider is a free mailbox provider. |
| `checks.mx` | string | MX lookup result. |
| `checks.role` | string | Role-address check result. |
| `checks.smtp` | string | SMTP verification result. |
| `checks.syntax` | string | Syntax validation result. |
| `credits_remaining` | number | Remaining monthly credits after the verification. |
| `details` | object | Additional verification details. |
| `details.catch_all` | boolean | Whether the domain is catch-all when available. |
| `details.catchAll` | boolean | Catch-all indicator returned by the API. |
| `details.has_typo_suggestion` | boolean | Whether MailCheck found a typo suggestion. |
| `details.is_disposable` | boolean | Whether the address uses a disposable provider. |
| `details.is_free_provider` | boolean | Whether the provider is free. |
| `details.is_role` | boolean | Whether the email is role-based. |
| `details.mxHost` | string | Resolved MX host when available. |
| `details.risk_level` | string | Risk level classification. |
| `email` | string | Verified email address. |
| `reason` | string | Verification verdict reason. |
| `score` | number | Confidence score from 0 to 100. |
| `valid` | boolean | Whether MailCheck considers the email deliverable. |

## Native endpoint

Through the native Mailcheck API, this operation is `POST /v1/verify` (base URL `https://api.mailcheck.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email.md) for the provider-specific parameters and requirements.

