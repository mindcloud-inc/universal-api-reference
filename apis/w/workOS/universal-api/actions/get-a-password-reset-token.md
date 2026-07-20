# WorkOS: Get a password reset token

Retrieves a password reset token from your WorkOS environment.

```
GET https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-a-password-reset-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-a-password-reset-token?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-a-password-reset-token?${params}`, {
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
| `id` | string | yes | The ID of the password reset token. |

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

Through the native WorkOS API, this operation is `GET /user_management/password_reset/{id}` (base URL `https://api.workos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-password-reset-token.md) for the provider-specific parameters and requirements.

