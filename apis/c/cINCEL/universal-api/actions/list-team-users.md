# CINCEL: List Team Users



```
GET https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/list-team-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CINCEL `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/list-team-users?connectionId=$CONNECTION_ID&limit=25&offset=0&team=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "team": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/list-team-users?${params}`, {
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
| `team` | string | yes | UUID of the team whose users should be listed. |
| `includeDeleted` | boolean | no | Include deleted users when true. |
| `nameLike` | string | no | Filter users by partial name match. |
| `emailLike` | string | no | Filter users by partial email match. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "curp": "string",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "job": "string",
      "name": "Ava Chen",
      "rfc": "string",
      "role": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the user is active. |
| `createdAt` | date | User creation timestamp. |
| `curp` | string | User CURP when present. |
| `deletedAt` | date | Deletion timestamp when the user has been deleted. |
| `email` | string | User email address. |
| `id` | string | User identifier. |
| `job` | string | User job title when present. |
| `name` | string | User display name. |
| `rfc` | string | User RFC when present. |
| `role` | string | User role within the team. |
| `updatedAt` | date | User last update timestamp. |

## Native endpoint

Through the native CINCEL API, this operation is `GET /teams/:team/users` (base URL `https://api.cincel.digital/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-team-users.md) for the provider-specific parameters and requirements.

