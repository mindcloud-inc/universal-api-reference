# Files.com: Get User

Finds a user in Files.com by ID.

```
GET https://connect.mindcloud.co/v1/universal/filescom/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Files.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filescom/latest/actions/get-user?connectionId=$CONNECTION_ID&id=1315585" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1315585"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filescom/latest/actions/get-user?${params}`, {
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
| `id` | number | yes | Numeric user ID. Default: `1315585`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "disabled": true,
      "email": "ava@example.com",
      "id": 1,
      "last_login_at": "2026-05-07T12:00:00.000Z",
      "restapi_permission": true,
      "site_admin": true,
      "time_zone": "string",
      "username": "Ava Chen",
      "workspace_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `disabled` | boolean |  |
| `email` | string |  |
| `id` | number |  |
| `last_login_at` | date |  |
| `restapi_permission` | boolean |  |
| `site_admin` | boolean |  |
| `time_zone` | string |  |
| `username` | string |  |
| `workspace_id` | number |  |

## Native endpoint

Through the native Files.com API, this operation is `GET /users/:id` (base URL `{{credentials.siteUrl}}/api/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

