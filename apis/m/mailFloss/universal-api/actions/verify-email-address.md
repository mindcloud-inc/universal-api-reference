# MailFloss: Verify Email Address

Verifies an email address with MailFloss.

```
GET https://connect.mindcloud.co/v1/universal/mailFloss/latest/actions/verify-email-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailFloss `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailFloss/latest/actions/verify-email-address?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailFloss/latest/actions/verify-email-address?${params}`, {
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
| `email` | string | yes | The email address to verify. |
| `timeout` | number | no | Timeout in milliseconds. Max 60000; defaults to 30000. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "disposable": true,
      "domain": "string",
      "email": "ava@example.com",
      "free": true,
      "meta": "string",
      "passed": true,
      "reason": "string",
      "role": true,
      "status": "string",
      "suggestion": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `disposable` | boolean | Whether the email uses a disposable domain. |
| `domain` | string | Email domain. |
| `email` | string | The checked email address. |
| `free` | boolean | Whether the email uses a free email provider. |
| `meta` | string | Additional meta information. |
| `passed` | boolean | Whether the email passed verification. |
| `reason` | string | Verification category. |
| `role` | boolean | Whether the email is role-based. |
| `status` | string | Verification status. |
| `suggestion` | string | Suggested email address, if available. |

## Native endpoint

Through the native MailFloss API, this operation is `GET /verify` (base URL `https://api.mailfloss.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email-address.md) for the provider-specific parameters and requirements.

