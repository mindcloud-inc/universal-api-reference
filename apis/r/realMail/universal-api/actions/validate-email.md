# RealMail: Validate Email

Validates an email address with RealMail.

```
GET https://connect.mindcloud.co/v1/universal/realMail/latest/actions/validate-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RealMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/realMail/latest/actions/validate-email?connectionId=$CONNECTION_ID&email=email%40domain.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "email@domain.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/realMail/latest/actions/validate-email?${params}`, {
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
| `email` | string | yes | Email address to validate. Example: `email@domain.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "free_email_provider": true,
      "has_active_website": true,
      "is_disposable": true,
      "is_suspected_role": true,
      "mx_found": true,
      "reason_code": "string",
      "reason_message": "string",
      "remaining_validations": 1,
      "suggestion": "string",
      "valid": true,
      "valid_email_format": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Validated email address. |
| `free_email_provider` | boolean | Whether the email comes from a free provider. |
| `has_active_website` | boolean | Whether the domain has an active website. |
| `is_disposable` | boolean | Whether the email appears disposable. |
| `is_suspected_role` | boolean | Whether the email looks like a role address. |
| `mx_found` | boolean | Whether the domain has a valid MX record. |
| `reason_code` | string | Validation reason code when the email is not valid. |
| `reason_message` | string | Human-readable validation reason. |
| `remaining_validations` | number | Remaining validations for the organization. |
| `suggestion` | string | Suggested corrected email when a domain typo is detected. |
| `valid` | boolean | Overall validation result. |
| `valid_email_format` | boolean | Whether the email format matches RFC-style validation. |

## Native endpoint

Through the native RealMail API, this operation is `POST /v1/validate` (base URL `https://api.realmail.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-email.md) for the provider-specific parameters and requirements.

