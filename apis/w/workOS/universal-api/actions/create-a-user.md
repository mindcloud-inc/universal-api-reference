# WorkOS: Create a user

Creates a user in your WorkOS environment.

```
POST https://connect.mindcloud.co/v1/universal/workOS/latest/actions/create-a-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/create-a-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workOS/latest/actions/create-a-user', {
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
| `email` | string | yes | The email address of the user. |
| `password` | string | no | The password to set for the user. Mutually exclusive with `password_hash` and `password_hash_type`. |
| `password_hash` | string | no | The hashed password to set for the user. Mutually exclusive with `password`. |
| `password_hash_type` | string | no | The algorithm originally used to hash the password, used when providing a `password_hash`. |
| `first_name` | string | no | The first name of the user. |
| `last_name` | string | no | The last name of the user. |
| `email_verified` | boolean | no | Whether the user's email has been verified. |
| `metadata` | object | no | Object containing metadata key/value pairs associated with the user. |
| `external_id` | string | no | The external ID of the user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "email_verified": true,
      "external_id": "string",
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen",
      "last_sign_in_at": "2026-05-07T12:00:00.000Z",
      "locale": "string",
      "message": "string",
      "metadata": {},
      "object": "string",
      "profile_picture_url": "https://example.com",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | An ISO 8601 timestamp. |
| `email` | string | The email address of the user. |
| `email_verified` | boolean | Whether the user's email has been verified. |
| `external_id` | string | The external ID of the user. |
| `first_name` | string | The first name of the user. |
| `id` | string | The unique ID of the user. |
| `last_name` | string | The last name of the user. |
| `last_sign_in_at` | date | The timestamp when the user last signed in. |
| `locale` | string | The user's preferred locale. |
| `message` | string | WorkOS response field message. |
| `metadata` | object | Object containing metadata key/value pairs associated with the user. |
| `object` | string | Distinguishes the user object. |
| `profile_picture_url` | string | A URL reference to an image representing the user. |
| `updated_at` | date | An ISO 8601 timestamp. |

## Native endpoint

Through the native WorkOS API, this operation is `POST /user_management/users` (base URL `https://api.workos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-user.md) for the provider-specific parameters and requirements.

