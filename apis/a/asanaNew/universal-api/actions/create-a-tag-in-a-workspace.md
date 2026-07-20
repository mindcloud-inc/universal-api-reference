# Asana: Create a tag in a workspace

Creates a tag in an Asana workspace.

```
POST https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/create-a-tag-in-a-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/create-a-tag-in-a-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": "string",
  "workspaceGid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/create-a-tag-in-a-workspace', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": "string",
    "workspaceGid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | string | yes |  |
| `workspaceGid` | string | yes |  |

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
      "color": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "gid": "string",
      "name": "Ava Chen",
      "notes": "string",
      "permalinkUrl": "https://example.com",
      "resourceType": "string",
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
| `color` | object |  |
| `createdAt` | date |  |
| `gid` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `permalinkUrl` | string |  |
| `resourceType` | string |  |
| `workspace.gid` | string |  |
| `workspace.name` | string |  |
| `workspace.resourceType` | string |  |

## Native endpoint

Through the native Asana API, this operation is `POST workspaces/:workspace_gid/tags` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-tag-in-a-workspace.md) for the provider-specific parameters and requirements.

