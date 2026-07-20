# Asana: Get workspace memberships for a user

Retrieves a user's workspace memberships from Asana.

```
GET https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-workspace-memberships-for-a-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-workspace-memberships-for-a-user?connectionId=$CONNECTION_ID&limit=25&offset=0&userGid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "userGid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-workspace-memberships-for-a-user?${params}`, {
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
| `userGid` | string | yes |  |

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
      "user": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceType": "string"
      },
      "workspace": {
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
| `user.gid` | string |  |
| `user.name` | string |  |
| `user.resourceType` | string |  |
| `workspace.gid` | string |  |
| `workspace.name` | string |  |
| `workspace.resourceType` | string |  |

## Native endpoint

Through the native Asana API, this operation is `GET users/:user_gid/workspace_memberships` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-workspace-memberships-for-a-user.md) for the provider-specific parameters and requirements.

