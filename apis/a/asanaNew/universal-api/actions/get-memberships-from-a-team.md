# Asana: Get memberships from a team

Retrieves team memberships from Asana.

```
GET https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-memberships-from-a-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-memberships-from-a-team?connectionId=$CONNECTION_ID&limit=25&offset=0&teamGid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "teamGid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-memberships-from-a-team?${params}`, {
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
| `teamGid` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `optPretty` | boolean | no |  |
| `optFields` | list<string> | no |  |

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

Through the native Asana API, this operation is `GET teams/:team_gid/team_memberships` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-memberships-from-a-team.md) for the provider-specific parameters and requirements.

