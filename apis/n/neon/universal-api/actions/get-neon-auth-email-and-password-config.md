# Neon: Get email and password configuration

Retrieves email and password configuration from Neon.

```
GET https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-neon-auth-email-and-password-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-neon-auth-email-and-password-config?connectionId=$CONNECTION_ID&project_id=string&branch_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string",
  "branch_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-neon-auth-email-and-password-config?${params}`, {
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
| `project_id` | string | yes | Neon API parameter project_id |
| `branch_id` | string | yes | Neon API parameter branch_id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auto_sign_in_after_verification": true,
      "disable_sign_up": true,
      "email_verification_method": [
        "ava@example.com"
      ],
      "enabled": true,
      "require_email_verification": true,
      "send_verification_email_on_sign_in": true,
      "send_verification_email_on_sign_up": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auto_sign_in_after_verification` | boolean |  |
| `disable_sign_up` | boolean |  |
| `email_verification_method` | array |  |
| `enabled` | boolean |  |
| `require_email_verification` | boolean |  |
| `send_verification_email_on_sign_in` | boolean |  |
| `send_verification_email_on_sign_up` | boolean |  |

## Native endpoint

Through the native Neon API, this operation is `GET /projects/:project_id/branches/:branch_id/auth/email_and_password` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-neon-auth-email-and-password-config.md) for the provider-specific parameters and requirements.

