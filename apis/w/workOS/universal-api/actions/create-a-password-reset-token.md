# WorkOS: Create a password reset token

Creates a password reset token in your WorkOS environment.

```
POST https://connect.mindcloud.co/v1/universal/workOS/latest/actions/create-a-password-reset-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/create-a-password-reset-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workOS/latest/actions/create-a-password-reset-token', {
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
| `email` | string | yes | The email address of the user requesting a password reset. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "expires_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "message": "string",
      "object": "string",
      "password_reset_token": "string",
      "password_reset_url": "https://example.com",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | The timestamp when the password reset token was created. |
| `email` | string | The email address of the user. |
| `expires_at` | date | The timestamp when the password reset token expires. |
| `id` | string | The unique ID of the password reset object. |
| `message` | string | WorkOS response field message. |
| `object` | string | Distinguishes the password reset object. |
| `password_reset_token` | string | The token used to reset the password. |
| `password_reset_url` | string | The URL where the user can reset their password. |
| `user_id` | string | The unique ID of the user. |

## Native endpoint

Through the native WorkOS API, this operation is `POST /user_management/password_reset` (base URL `https://api.workos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-password-reset-token.md) for the provider-specific parameters and requirements.

