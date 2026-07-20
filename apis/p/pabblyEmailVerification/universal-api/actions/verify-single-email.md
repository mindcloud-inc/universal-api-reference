# Pabbly Email Verification: Verify Single Email



```
GET https://connect.mindcloud.co/v1/universal/pabblyEmailVerification/latest/actions/verify-single-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Email Verification `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblyEmailVerification/latest/actions/verify-single-email?connectionId=$CONNECTION_ID&email=johnfabric%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "johnfabric@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblyEmailVerification/latest/actions/verify-single-email?${params}`, {
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
| `email` | string | yes | Email address to verify. Example: `johnfabric@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "accept_all": 1,
        "disposable": 1,
        "domain": "string",
        "email": "ava@example.com",
        "free_email": 1,
        "message": "string",
        "result": "string",
        "role": 1,
        "spamtrap": 1,
        "success": true,
        "user": "string"
      },
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.accept_all` | number | Whether the domain accepts all mail, returned as 0 or 1. |
| `data.disposable` | number | Whether the email is disposable, returned as 0 or 1. |
| `data.domain` | string | Domain part of the email address. |
| `data.email` | string | Email address that was verified. |
| `data.free_email` | number | Whether the address is a free email provider address, returned as 0 or 1. |
| `data.message` | string | Detailed result message. |
| `data.result` | string | Verification result for the email address. |
| `data.role` | number | Whether the email is role-based, returned as 0 or 1. |
| `data.spamtrap` | number | Whether the email is detected as a spam trap, returned as 0 or 1. |
| `data.success` | boolean | Whether validation succeeded. |
| `data.user` | string | Mailbox/user part of the email address. |
| `message` | string | Top-level response message. |
| `status` | string | Top-level request status. |

## Native endpoint

Through the native Pabbly Email Verification API, this operation is `POST /email-lists/verify-single` (base URL `https://verify.pabbly.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-single-email.md) for the provider-specific parameters and requirements.

