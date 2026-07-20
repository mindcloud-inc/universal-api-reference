# Neon: Update email and password configuration

Updates email and password configuration in Neon.

```
PUT https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-neon-auth-email-and-password-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-neon-auth-email-and-password-config" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "string",
  "branch_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-neon-auth-email-and-password-config', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "string",
    "branch_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project_id` | string | yes | Neon API parameter project_id |
| `branch_id` | string | yes | Neon API parameter branch_id |
| `enabled` | boolean | no | Neon API parameter enabled |
| `email_verification_method` | list | no | Neon API parameter email_verification_method One of: `0`, `1`. |
| `require_email_verification` | boolean | no | Neon API parameter require_email_verification |
| `auto_sign_in_after_verification` | boolean | no | Neon API parameter auto_sign_in_after_verification |
| `send_verification_email_on_sign_up` | boolean | no | Neon API parameter send_verification_email_on_sign_up |
| `send_verification_email_on_sign_in` | boolean | no | Neon API parameter send_verification_email_on_sign_in |
| `disable_sign_up` | boolean | no | Neon API parameter disable_sign_up |

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

Through the native Neon API, this operation is `PATCH /projects/:project_id/branches/:branch_id/auth/email_and_password` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-neon-auth-email-and-password-config.md) for the provider-specific parameters and requirements.

