# SuperSend: Verify Email (SMTP)

Verifies an email in SuperSend using SMTP.

```
POST https://connect.mindcloud.co/v1/universal/superSend/latest/actions/verify-email-smtp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/verify-email-smtp" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superSend/latest/actions/verify-email-smtp', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes |  |
| `teamId` | string | no | Optional team UUID for credit transaction attribution |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bounce_type_breakdown": {},
      "confidence": "string",
      "credits_used": 1,
      "domain": "string",
      "email": "ava@example.com",
      "email_hash": "ava@example.com",
      "email_provider": "ava@example.com",
      "email_security_service": "ava@example.com",
      "hard_bounce_count": 1,
      "has_historical_data": true,
      "is_abuse_email": true,
      "is_disallowed": true,
      "is_free_provider": true,
      "is_role_based": true,
      "reply_count": 1,
      "risk_level": "string",
      "total_sends": 1,
      "valid": true,
      "validators": {},
      "validity_score": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounce_type_breakdown` | object |  |
| `confidence` | string |  |
| `credits_used` | number |  |
| `domain` | string |  |
| `email` | string |  |
| `email_hash` | string |  |
| `email_provider` | string |  |
| `email_security_service` | string |  |
| `hard_bounce_count` | number |  |
| `has_historical_data` | boolean |  |
| `is_abuse_email` | boolean |  |
| `is_disallowed` | boolean |  |
| `is_free_provider` | boolean |  |
| `is_role_based` | boolean |  |
| `reply_count` | number |  |
| `risk_level` | string |  |
| `total_sends` | number |  |
| `valid` | boolean |  |
| `validators` | object |  |
| `validity_score` | number |  |

## Native endpoint

Through the native SuperSend API, this operation is `POST /email-validation/verify` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email-smtp.md) for the provider-specific parameters and requirements.

