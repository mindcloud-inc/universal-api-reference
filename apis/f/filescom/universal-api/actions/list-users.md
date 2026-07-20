# Files.com: List Users

Retrieves user accounts from a Files.com site.

```
GET https://connect.mindcloud.co/v1/universal/filescom/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Files.com `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filescom/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filescom/latest/actions/list-users?${params}`, {
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
| `includeParentSiteUsers` | boolean | no | Include users inherited from the parent site. |
| `perPage` | number | no | Maximum number of items to return in one page. |
| `cursor` | string | no | Cursor token returned by a previous page. |
| `search` | string | no | Search users by text. |

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
| `username` | string |  |
| `workspace_id` | number |  |

## Native endpoint

Through the native Files.com API, this operation is `GET /users` (base URL `{{credentials.siteUrl}}/api/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

