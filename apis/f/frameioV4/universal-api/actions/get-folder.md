# Frame.io v4: Get Folder

Retrieves a folder from Frame.io v4.

```
GET https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/get-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frame.io v4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/get-folder?connectionId=$CONNECTION_ID&accountId=string&folderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "folderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/get-folder?${params}`, {
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
| `folderId` | string | yes |  |
| `include` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "coverFileId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creator": {
        "active": true,
        "adobeUserId": "string",
        "avatarUrl": "https://example.com",
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "id": "string",
      "metadata": [
        [
          {}
        ]
      ],
      "name": "Ava Chen",
      "parentId": "string",
      "project": {
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
      },
      "projectId": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "viewUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `coverFileId` | string | Cover asset ID |
| `createdAt` | date | Creation timestamp |
| `creator` | object | User details |
| `creator.active` | boolean | User active status |
| `creator.adobeUserId` | string | Adobe user ID |
| `creator.avatarUrl` | string | User avatar image url |
| `creator.email` | string | User email |
| `creator.id` | string | User ID - can be null for invited users with no frame account |
| `creator.name` | string | User name |
| `id` | string | File, Folder, or Version Stack ID |
| `metadata[]` | array<object> | File attributes |
| `metadata[].customMembers[]` | array<object> | Populated with custom member options only if `member_options_type` is set to 'custom'. |
| `metadata[].customMembers[].id` | string | User Id or Account User Group Id |
| `metadata[].customMembers[].type` | string |  |
| `metadata[].fieldDefinitionId` | string | Field definition ID |
| `metadata[].fieldDefinitionName` | string | Field definition name |
| `metadata[].fieldOptions[]` | array<object> |  |
| `metadata[].fieldOptions[].displayName` | string | Option display name |
| `metadata[].fieldOptions[].id` | string | Option ID |
| `metadata[].fieldType` | string | Field type |
| `metadata[].memberOptionsType` | string |  |
| `metadata[].mutable` | boolean | Metadata mutability. System field values cannot be updated. |
| `metadata[].value[]` | array<object> |  |
| `metadata[].value[].id` | string | User Id or Account User Group Id |
| `metadata[].value[].type` | string |  |
| `name` | string | File or Folder Name |
| `parentId` | string | Parent Folder or Version Stack ID |
| `project` | object | Frame.io Project |
| `project.createdAt` | date | Created Timestamp |
| `project.description` | string | Project Description |
| `project.id` | string | Project ID |
| `project.name` | string | Project Name |
| `project.owner` | object | User details |
| `project.owner.active` | boolean | User active status |
| `project.owner.adobeUserId` | string | Adobe user ID |
| `project.owner.avatarUrl` | string | User avatar image url |
| `project.owner.email` | string | User email |
| `project.owner.id` | string | User ID - can be null for invited users with no frame account |
| `project.owner.name` | string | User name |
| `project.restricted` | boolean | Whether the project is restricted or not |
| `project.rootFolderId` | string | Root Folder ID |
| `project.status` | string | Project Status |
| `project.storage` | number | Storage Usage |
| `project.updatedAt` | date | Updated Timestamp |
| `project.viewUrl` | string | URL to view the project in the Frame.io web application |
| `project.workspaceId` | string | Workspace ID |
| `projectId` | string | Project ID |
| `type` | string |  |
| `updatedAt` | date | Update timestamp |
| `viewUrl` | string | URL to view the asset in the Frame.io web application |

## Native endpoint

Through the native Frame.io v4 API, this operation is `GET /accounts/:accountId/folders/:folderId` (base URL `https://api.frame.io/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-folder.md) for the provider-specific parameters and requirements.

