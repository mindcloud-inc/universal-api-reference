# WorkOS: Get a user

Retrieves a user from your WorkOS environment.

```
GET https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-a-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-a-user?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-a-user?${params}`, {
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
| `id` | string | yes | The unique ID of the user. |

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

Through the native WorkOS API, this operation is `GET /user_management/users/{id}` (base URL `https://api.workos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-user.md) for the provider-specific parameters and requirements.

