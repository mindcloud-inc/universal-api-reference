# CINCEL: List User Teams



```
GET https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/list-user-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CINCEL `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/list-user-teams?connectionId=$CONNECTION_ID&limit=25&offset=0&user=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "user": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/list-user-teams?${params}`, {
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
| `user` | number | yes | User ID whose teams should be listed. |
| `includeDeleted` | boolean | no | Include deleted teams when true. |
| `nameLike` | string | no | Filter teams by partial name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "deletedAt": {},
      "emoji": {},
      "isDefaultTeam": true,
      "logo": "string",
      "name": "Ava Chen",
      "role": "string",
      "updatedAt": "string",
      "uuid": "string",
      "workspace": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `deletedAt` | object |  |
| `emoji` | object |  |
| `isDefaultTeam` | boolean |  |
| `logo` | string |  |
| `name` | string |  |
| `role` | string |  |
| `updatedAt` | string |  |
| `uuid` | string |  |
| `workspace` | object |  |

## Native endpoint

Through the native CINCEL API, this operation is `GET /users/:user/teams` (base URL `https://api.cincel.digital/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-teams.md) for the provider-specific parameters and requirements.

