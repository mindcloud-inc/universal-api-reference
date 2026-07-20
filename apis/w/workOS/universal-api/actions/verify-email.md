# WorkOS: Verify email

Verifies an email in your WorkOS environment.

```
POST https://connect.mindcloud.co/v1/universal/workOS/latest/actions/verify-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/verify-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "code": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workOS/latest/actions/verify-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "code": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ID of the user. |
| `code` | string | yes | The one-time email verification code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": "string",
      "object": "string",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | WorkOS response field id. |
| `message` | string | WorkOS response field message. |
| `object` | string | WorkOS response field object. |
| `user` | object | The user whose email was verified. |

## Native endpoint

Through the native WorkOS API, this operation is `POST /user_management/users/{id}/email_verification/confirm` (base URL `https://api.workos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email.md) for the provider-specific parameters and requirements.

