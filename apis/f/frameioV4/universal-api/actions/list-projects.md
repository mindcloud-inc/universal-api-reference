# Frame.io v4: List Projects

Retrieves projects from a workspace in Frame.io v4.

```
GET https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frame.io v4 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=string&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "string",
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/list-projects?${params}`, {
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
| `accountId` | string | yes |  |
| `workspaceId` | string | yes |  |
| `include` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "owner": {
        "active": true,
        "adobeUserId": "string",
        "avatarUrl": "https://example.com",
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
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
| `description` | string | Project Description |
| `id` | string | Project ID |
| `name` | string | Project Name |
| `owner` | object | User details |
| `owner.active` | boolean | User active status |
| `owner.adobeUserId` | string | Adobe user ID |
| `owner.avatarUrl` | string | User avatar image url |
| `owner.email` | string | User email |
| `owner.id` | string | User ID - can be null for invited users with no frame account |
| `owner.name` | string | User name |
| `restricted` | boolean | Whether the project is restricted or not |
| `rootFolderId` | string | Root Folder ID |
| `status` | string | Project Status |
| `storage` | number | Storage Usage |
| `updatedAt` | date | Updated Timestamp |
| `viewUrl` | string | URL to view the project in the Frame.io web application |
| `workspaceId` | string | Workspace ID |

## Native endpoint

Through the native Frame.io v4 API, this operation is `GET /accounts/:accountId/workspaces/:workspaceId/projects` (base URL `https://api.frame.io/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

