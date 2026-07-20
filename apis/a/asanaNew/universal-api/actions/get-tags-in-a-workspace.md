# Asana: Get tags in a workspace

Retrieves tags in an Asana workspace.

```
GET https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-tags-in-a-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-tags-in-a-workspace?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceGid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspaceGid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-tags-in-a-workspace?${params}`, {
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
| `workspaceGid` | string | yes | Asana workspace gid parameter. |
| `opt_pretty` | boolean | no | Asana opt pretty parameter. |
| `limit` | number | no | Asana limit parameter. |
| `offset` | string | no | Asana offset parameter. |
| `opt_fields` | list<string> | no | Asana opt fields parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "gid": "string",
      "name": "Ava Chen",
      "resourceType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gid` | string |  |
| `name` | string |  |
| `resourceType` | string |  |

## Native endpoint

Through the native Asana API, this operation is `GET workspaces/:workspace_gid/tags` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-tags-in-a-workspace.md) for the provider-specific parameters and requirements.

