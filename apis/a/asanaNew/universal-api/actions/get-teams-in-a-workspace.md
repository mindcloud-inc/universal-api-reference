# Asana: Get teams in a workspace

Retrieves teams in an Asana workspace.

```
GET https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-teams-in-a-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-teams-in-a-workspace?connectionId=$CONNECTION_ID&workspaceGid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceGid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-teams-in-a-workspace?${params}`, {
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
| `optFields[]` | array<string> | no |  |
| `workspaceGid` | string | yes | Path parameter: workspace_gid |

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

Through the native Asana API, this operation is `GET workspaces/:workspace_gid/teams` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-teams-in-a-workspace.md) for the provider-specific parameters and requirements.

