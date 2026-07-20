# Asana: Get memberships from a user

Retrieves team memberships for a user from Asana.

```
GET https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-memberships-from-a-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-memberships-from-a-user?connectionId=$CONNECTION_ID&limit=25&offset=0&userGid=string&workspace=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "userGid": "string",
  "workspace": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-memberships-from-a-user?${params}`, {
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
| `userGid` | string | yes | Asana user gid parameter. |
| `opt_pretty` | boolean | no | Asana opt pretty parameter. |
| `limit` | number | no | Asana limit parameter. |
| `offset` | string | no | Asana offset parameter. |
| `workspace` | string | yes | Asana workspace parameter. |
| `opt_fields` | list<string> | no | Asana opt fields parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "gid": "string",
      "resourceType": "string",
      "team": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceType": "string"
      },
      "user": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceType": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gid` | string |  |
| `resourceType` | string |  |
| `team.gid` | string |  |
| `team.name` | string |  |
| `team.resourceType` | string |  |
| `user.gid` | string |  |
| `user.name` | string |  |
| `user.resourceType` | string |  |

## Native endpoint

Through the native Asana API, this operation is `GET users/:user_gid/team_memberships` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-memberships-from-a-user.md) for the provider-specific parameters and requirements.

