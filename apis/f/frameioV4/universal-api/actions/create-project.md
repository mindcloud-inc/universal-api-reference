# Frame.io v4: Create Project

Creates a new project in Frame.io v4.

```
POST https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frame.io v4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "workspaceId": "string",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "workspaceId": "string",
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes |  |
| `workspaceId` | string | yes |  |
| `data` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "restricted": true,
      "rootFolderId": "string",
      "status": "string",
      "storage": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "viewUrl": "https://example.com",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Created Timestamp |
| `id` | string | Project ID |
| `name` | string | Project Name |
| `restricted` | boolean | Whether the project is restricted or not |
| `rootFolderId` | string | Root Folder ID |
| `status` | string | Project Status |
| `storage` | number | Storage Usage |
| `updatedAt` | date | Updated Timestamp |
| `viewUrl` | string | URL to view the project in the Frame.io web application |
| `workspaceId` | string | Workspace ID |

## Native endpoint

Through the native Frame.io v4 API, this operation is `POST /accounts/:accountId/workspaces/:workspaceId/projects` (base URL `https://api.frame.io/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

