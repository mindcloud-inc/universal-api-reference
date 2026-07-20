# Mailcheck: Bulk Verify Emails



```
POST https://connect.mindcloud.co/v1/universal/mailcheck/latest/actions/bulk-verify-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailcheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailcheck/latest/actions/bulk-verify-emails" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails[]": [
    "ava@example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailcheck/latest/actions/bulk-verify-emails', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails[]": ["ava@example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emails[]` | array<string> | yes | Up to 100 email addresses to verify in one request. Provide a JSON array of email strings. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookUrl` | string | no | Optional HTTPS URL that MailCheck should notify when bulk verification completes. Example: `https://your-server.example.com/mailcheck/webhook`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits_remaining": 1,
      "job_id": "string",
      "results": [
        [
          {}
        ]
      ],
      "total": 1,
      "unique_verified": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits_remaining` | number | Remaining monthly credits after the bulk verification. |
| `job_id` | string | Bulk verification job identifier. |
| `results[]` | array<object> | Verification results in input order. |
| `results[].cached` | boolean | Whether the result came from cache. |
| `results[].checks` | object | Per-check outcomes for the email. |
| `results[].checks.disposable` | string | Disposable-email check result. |
| `results[].checks.free_provider` | boolean | Whether the provider is free. |
| `results[].checks.mx` | string | MX lookup result. |
| `results[].checks.role` | string | Role-address check result. |
| `results[].checks.smtp` | string | SMTP verification result. |
| `results[].checks.syntax` | string | Syntax validation result. |
| `results[].details` | object | Additional verification details. |
| `results[].details.catch_all` | boolean | Whether the domain is catch-all when available. |
| `results[].details.catchAll` | boolean | Catch-all indicator returned by the API. |
| `results[].details.has_typo_suggestion` | boolean | Whether MailCheck found a typo suggestion. |
| `results[].details.is_disposable` | boolean | Whether the address uses a disposable provider. |
| `results[].details.is_free_provider` | boolean | Whether the provider is free. |
| `results[].details.is_role` | boolean | Whether the email is role-based. |
| `results[].details.mxHost` | string | Resolved MX host when available. |
| `results[].details.risk_level` | string | Risk level classification. |
| `results[].details.role` | string | Detected role mailbox when available. |
| `results[].email` | string | Verified email address. |
| `results[].reason` | string | Verification verdict reason. |
| `results[].score` | number | Confidence score from 0 to 100. |
| `results[].valid` | boolean | Whether MailCheck considers the email deliverable. |
| `total` | number | Total number of results returned. |
| `unique_verified` | number | Number of unique email addresses verified. |

## Native endpoint

Through the native Mailcheck API, this operation is `POST /v1/verify/bulk` (base URL `https://api.mailcheck.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-verify-emails.md) for the provider-specific parameters and requirements.

