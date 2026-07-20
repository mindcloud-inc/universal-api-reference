# Asana: Add a user to a workspace or organization

Adds a user to an Asana workspace or organization.

```
POST https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/add-a-user-to-a-workspace-or-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/add-a-user-to-a-workspace-or-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dataUser": "string",
  "workspaceGid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/add-a-user-to-a-workspace-or-organization', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dataUser": "string",
    "workspaceGid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataUser` | string | yes |  |
| `workspaceGid` | string | yes | Asana workspace gid parameter. |
| `opt_pretty` | boolean | no | Asana opt pretty parameter. |
| `opt_fields` | list<string> | no | Asana opt fields parameter. |
| `data.user` | string | no | Asana user parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "gid": "string",
      "name": "Ava Chen",
      "photo": {},
      "resourceType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `gid` | string |  |
| `name` | string |  |
| `photo` | object |  |
| `resourceType` | string |  |

## Native endpoint

Through the native Asana API, this operation is `POST workspaces/:workspace_gid/addUser` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-a-user-to-a-workspace-or-organization.md) for the provider-specific parameters and requirements.

