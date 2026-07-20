# Shuffll: Update Workspace

Updates an existing workspace in Shuffll.

```
PUT https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/update-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffll `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/update-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "organizationId": "69cac8104c4a701fd26271a1",
  "workspaceId": "69cac8104c4a701fd26271a5"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/update-workspace', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "organizationId": "69cac8104c4a701fd26271a1",
    "workspaceId": "69cac8104c4a701fd26271a5"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | New workspace name. |
| `organizationId` | string | yes | Shuffll organization id. Default: `69cac8104c4a701fd26271a1`. |
| `workspaceId` | string | yes | Shuffll workspace id. Default: `69cac8104c4a701fd26271a5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assetCount": 1,
      "branding": {},
      "createdByEmail": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "projectCount": 1,
      "templateCount": 1,
      "userCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assetCount` | number | Asset count. |
| `branding` | object | Workspace branding. |
| `createdByEmail` | string | Creator email. |
| `id` | string | Workspace id. |
| `name` | string | Workspace name. |
| `projectCount` | number | Project count. |
| `templateCount` | number | Template count. |
| `userCount` | number | Workspace user count. |

## Native endpoint

Through the native Shuffll API, this operation is `PUT /auth/organization/:organizationId/workspace/:workspaceId` (base URL `https://api.shuffll.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workspace.md) for the provider-specific parameters and requirements.

