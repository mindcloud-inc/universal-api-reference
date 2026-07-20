# Zenkit: Create Workspace

Creates a new workspace in Zenkit.

```
POST https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/create-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/create-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/create-workspace', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "access": {
        "groupId": "string",
        "roleId": "string",
        "userId": 1,
        "uuid": "string",
        "workspaceId": 1
      },
      "workspace": {
        "appType": "string",
        "backgroundId": "string",
        "coverImageId": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "created_by": 1,
        "deprecated_at": "string",
        "description": "string",
        "iconBackgroundColor": "string",
        "iconClassNames": "Ava Chen",
        "iconColor": "string",
        "id": 1,
        "imageId": "string",
        "isDefault": true,
        "name": "Ava Chen",
        "organizationId": 1,
        "parentWorkspaceId": "string",
        "resourceType": "string",
        "shortId": "string",
        "sortOrder": "string",
        "transferOrganizationCount": 1,
        "transferOwnershipCount": 1,
        "updated_at": "2026-05-07T12:00:00.000Z",
        "uuid": "string",
        "visibility": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access.groupId` | string |  |
| `access.roleId` | string |  |
| `access.userId` | number |  |
| `access.uuid` | string |  |
| `access.workspaceId` | number |  |
| `workspace.appType` | string |  |
| `workspace.backgroundId` | string |  |
| `workspace.coverImageId` | string |  |
| `workspace.created_at` | date |  |
| `workspace.created_by` | number |  |
| `workspace.deprecated_at` | string |  |
| `workspace.description` | string |  |
| `workspace.iconBackgroundColor` | string |  |
| `workspace.iconClassNames` | string |  |
| `workspace.iconColor` | string |  |
| `workspace.id` | number |  |
| `workspace.imageId` | string |  |
| `workspace.isDefault` | boolean |  |
| `workspace.name` | string |  |
| `workspace.organizationId` | number |  |
| `workspace.parentWorkspaceId` | string |  |
| `workspace.resourceType` | string |  |
| `workspace.shortId` | string |  |
| `workspace.sortOrder` | string |  |
| `workspace.transferOrganizationCount` | number |  |
| `workspace.transferOwnershipCount` | number |  |
| `workspace.updated_at` | date |  |
| `workspace.uuid` | string |  |
| `workspace.visibility` | number |  |

## Native endpoint

Through the native Zenkit API, this operation is `POST /workspaces` (base URL `https://zenkit.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workspace.md) for the provider-specific parameters and requirements.

