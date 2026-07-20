# Codeberg: List User Teams



```
GET https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-user-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codeberg `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-user-teams?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-user-teams?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "can_create_org_repo": true,
      "description": "string",
      "id": 1,
      "includes_all_repositories": true,
      "name": "Ava Chen",
      "organization": {
        "id": 1,
        "name": "Ava Chen",
        "username": "Ava Chen"
      },
      "permission": "string",
      "units": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `can_create_org_repo` | boolean |  |
| `description` | string |  |
| `id` | number |  |
| `includes_all_repositories` | boolean |  |
| `name` | string |  |
| `organization.id` | number |  |
| `organization.name` | string |  |
| `organization.username` | string |  |
| `permission` | string |  |
| `units` | array<string> |  |

## Native endpoint

Through the native Codeberg API, this operation is `GET /user/teams` (base URL `https://codeberg.org/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-teams.md) for the provider-specific parameters and requirements.

