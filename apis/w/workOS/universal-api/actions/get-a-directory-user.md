# WorkOS: Get a Directory User

Retrieves a directory user from your WorkOS environment.

```
GET https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-a-directory-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-a-directory-user?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-a-directory-user?${params}`, {
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
| `id` | string | yes | Unique identifier for the Directory User. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "directory_id": "string",
      "email": "ava@example.com",
      "emails": [
        {}
      ],
      "first_name": "Ava",
      "id": "string",
      "idp_id": "string",
      "job_title": "string",
      "last_name": "Chen",
      "message": "string",
      "object": "string",
      "organization_id": "string",
      "state": "string",
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
| `directory_id` | string | The identifier of the Directory the Directory User belongs to. |
| `email` | string | The email address of the user. |
| `emails` | array<object> | A list of email addresses for the user. |
| `first_name` | string | The first name of the user. |
| `id` | string | Unique identifier for the Directory User. |
| `idp_id` | string | Unique identifier for the user, assigned by the Directory Provider. Different Directory Providers use different ID formats. |
| `job_title` | string | The job title of the user. |
| `last_name` | string | The last name of the user. |
| `message` | string | WorkOS response field message. |
| `object` | string | Distinguishes the Directory User object. |
| `organization_id` | string | The identifier for the Organization in which the Directory resides. |
| `state` | string | The state of the user. |
| `updated_at` | date | An ISO 8601 timestamp. |

## Native endpoint

Through the native WorkOS API, this operation is `GET /directory_users/{id}` (base URL `https://api.workos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-directory-user.md) for the provider-specific parameters and requirements.

