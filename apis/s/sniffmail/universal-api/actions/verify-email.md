# Sniffmail: Verify Email

Retrieves email verification results from Sniffmail.

```
GET https://connect.mindcloud.co/v1/universal/sniffmail/latest/actions/verify-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sniffmail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sniffmail/latest/actions/verify-email?connectionId=$CONNECTION_ID&email=test%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "test@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sniffmail/latest/actions/verify-email?${params}`, {
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
| `email` | string | yes | Enter the email address you want Sniffmail to verify. Example: `test@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "is_deliverable": true,
      "is_disposable": true,
      "is_reachable": "string",
      "is_role_account": true,
      "is_valid": true,
      "mx_valid": true,
      "reason": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | The email address that was verified. |
| `is_deliverable` | boolean | Whether the mailbox appears deliverable. |
| `is_disposable` | boolean | Whether the address belongs to a disposable email provider. |
| `is_reachable` | string | Sniffmail reachability classification for the email address. |
| `is_role_account` | boolean | Whether the address is a role inbox such as support@ or info@. |
| `is_valid` | boolean | Whether Sniffmail considers the address valid overall. |
| `mx_valid` | boolean | Whether the domain has valid MX records. |
| `reason` | string | Human-readable verification result reason. |

## Native endpoint

Through the native Sniffmail API, this operation is `POST /verify` (base URL `https://api.sniffmail.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email.md) for the provider-specific parameters and requirements.

