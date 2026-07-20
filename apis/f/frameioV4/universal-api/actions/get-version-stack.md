# Frame.io v4: Get Version Stack

Retrieves a version stack from Frame.io v4.

```
GET https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/get-version-stack
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frame.io v4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/get-version-stack?connectionId=$CONNECTION_ID&accountId=string&versionStackId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "versionStackId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/get-version-stack?${params}`, {
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
| `versionStackId` | string | yes |  |
| `include` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creator": {
        "active": true,
        "adobeUserId": "string",
        "avatarUrl": "https://example.com",
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "headVersion": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "creator": {
          "active": true,
          "adobeUserId": "string",
          "avatarUrl": "https://example.com",
          "email": "ava@example.com",
          "id": "string",
          "name": "Ava Chen"
        },
        "fileSize": 1,
        "id": "string",
        "mediaLinks": {
          "efficient": {
            "downloadUrl": "https://example.com"
          },
          "highQuality": {
            "downloadUrl": "https://example.com"
          },
          "original": {
            "downloadUrl": "https://example.com",
            "inlineUrl": "https://example.com"
          },
          "scrubSheet": {
            "downloadUrl": "https://example.com",
            "url": "https://example.com"
          },
          "thumbnail": {
            "downloadUrl": "https://example.com",
            "url": "https://example.com"
          },
          "thumbnailHighQuality": {
            "downloadUrl": "https://example.com",
            "url": "https://example.com"
          },
          "videoH264180": {
            "downloadUrl": "https://example.com",
            "url": "https://example.com"
          }
        },
        "mediaType": "string",
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
        "status": "string",
        "type": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "viewUrl": "https://example.com"
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
| `createdAt` | date | Creation timestamp |
| `creator` | object | User details |
| `creator.active` | boolean | User active status |
| `creator.adobeUserId` | string | Adobe user ID |
| `creator.avatarUrl` | string | User avatar image url |
| `creator.email` | string | User email |
| `creator.id` | string | User ID - can be null for invited users with no frame account |
| `creator.name` | string | User name |
| `headVersion` | object |  |
| `headVersion.createdAt` | date | Creation timestamp |
| `headVersion.creator` | object | User details |
| `headVersion.creator.active` | boolean | User active status |
| `headVersion.creator.adobeUserId` | string | Adobe user ID |
| `headVersion.creator.avatarUrl` | string | User avatar image url |
| `headVersion.creator.email` | string | User email |
| `headVersion.creator.id` | string | User ID - can be null for invited users with no frame account |
| `headVersion.creator.name` | string | User name |
| `headVersion.fileSize` | number | File size in bytes |
| `headVersion.id` | string | File, Folder, or Version Stack ID |
| `headVersion.mediaLinks` | object |  |
| `headVersion.mediaLinks.efficient` | object |  |
| `headVersion.mediaLinks.efficient.downloadUrl` | string | URL to download the media file.<br/> HTTP response headers will include Content-Disposition = 'attachment;filename=<filename>'.<br/> Watermarks may be applied for transcode links as per Account settings and User permissions.<br/> |
| `headVersion.mediaLinks.highQuality` | object |  |
| `headVersion.mediaLinks.highQuality.downloadUrl` | string | URL to download the media file.<br/> HTTP response headers will include Content-Disposition = 'attachment;filename=<filename>'.<br/> Watermarks may be applied for transcode links as per Account settings and User permissions.<br/> |
| `headVersion.mediaLinks.original` | object |  |
| `headVersion.mediaLinks.original.downloadUrl` | string | URL to download the media file.<br/> HTTP response headers will include Content-Disposition = 'attachment;filename=<filename>'.<br/> Watermarks may be applied for transcode links as per Account settings and User permissions.<br/> |
| `headVersion.mediaLinks.original.inlineUrl` | string | URL to view the media file in a web browser in its original resolution and media type.<br/> HTTP response headers will include Content-Disposition = 'inline;filename=<filename>'.<br/> |
| `headVersion.mediaLinks.scrubSheet` | object |  |
| `headVersion.mediaLinks.scrubSheet.downloadUrl` | string | URL to download the media file.<br/> HTTP response headers will include Content-Disposition = 'attachment;filename=<filename>'.<br/> Watermarks may be applied for transcode links as per Account settings and User permissions.<br/> |
| `headVersion.mediaLinks.scrubSheet.url` | string | URL to transcoded media that won't include any Content-Disposition header in the response.<br/> Watermarks may be applied as per Account settings and User permissions.<br/> Media content may be streamed (e.g. when watermarks are required). Clients may issue a HEAD request to determine whether Content-Length and/or Accept-Ranges headers are present in order to determine whether the content can be downloaded in parallel chunks. |
| `headVersion.mediaLinks.thumbnail` | object |  |
| `headVersion.mediaLinks.thumbnail.downloadUrl` | string | URL to download the media file.<br/> HTTP response headers will include Content-Disposition = 'attachment;filename=<filename>'.<br/> Watermarks may be applied for transcode links as per Account settings and User permissions.<br/> |
| `headVersion.mediaLinks.thumbnail.url` | string | URL to transcoded media that won't include any Content-Disposition header in the response.<br/> Watermarks may be applied as per Account settings and User permissions.<br/> Media content may be streamed (e.g. when watermarks are required). Clients may issue a HEAD request to determine whether Content-Length and/or Accept-Ranges headers are present in order to determine whether the content can be downloaded in parallel chunks. |
| `headVersion.mediaLinks.thumbnailHighQuality` | object |  |
| `headVersion.mediaLinks.thumbnailHighQuality.downloadUrl` | string | URL to download the media file.<br/> HTTP response headers will include Content-Disposition = 'attachment;filename=<filename>'.<br/> Watermarks may be applied for transcode links as per Account settings and User permissions.<br/> |
| `headVersion.mediaLinks.thumbnailHighQuality.url` | string | URL to transcoded media that won't include any Content-Disposition header in the response.<br/> Watermarks may be applied as per Account settings and User permissions.<br/> Media content may be streamed (e.g. when watermarks are required). Clients may issue a HEAD request to determine whether Content-Length and/or Accept-Ranges headers are present in order to determine whether the content can be downloaded in parallel chunks. |
| `headVersion.mediaLinks.videoH264180` | object |  |
| `headVersion.mediaLinks.videoH264180.downloadUrl` | string | URL to download the media file.<br/> HTTP response headers will include Content-Disposition = 'attachment;filename=<filename>'.<br/> Watermarks may be applied for transcode links as per Account settings and User permissions.<br/> |
| `headVersion.mediaLinks.videoH264180.url` | string | URL to transcoded media that won't include any Content-Disposition header in the response.<br/> Watermarks may be applied as per Account settings and User permissions.<br/> Media content may be streamed (e.g. when watermarks are required). Clients may issue a HEAD request to determine whether Content-Length and/or Accept-Ranges headers are present in order to determine whether the content can be downloaded in parallel chunks. |
| `headVersion.mediaType` | string | File media type |
| `headVersion.metadata[]` | array<object> | File attributes |
| `headVersion.metadata[].customMembers[]` | array<object> | Populated with custom member options only if `member_options_type` is set to 'custom'. |
| `headVersion.metadata[].customMembers[].id` | string | User Id or Account User Group Id |
| `headVersion.metadata[].customMembers[].type` | string |  |
| `headVersion.metadata[].fieldDefinitionId` | string | Field definition ID |
| `headVersion.metadata[].fieldDefinitionName` | string | Field definition name |
| `headVersion.metadata[].fieldOptions[]` | array<object> |  |
| `headVersion.metadata[].fieldOptions[].displayName` | string | Option display name |
| `headVersion.metadata[].fieldOptions[].id` | string | Option ID |
| `headVersion.metadata[].fieldType` | string | Field type |
| `headVersion.metadata[].memberOptionsType` | string |  |
| `headVersion.metadata[].mutable` | boolean | Metadata mutability. System field values cannot be updated. |
| `headVersion.metadata[].value[]` | array<object> |  |
| `headVersion.metadata[].value[].id` | string | User Id or Account User Group Id |
| `headVersion.metadata[].value[].type` | string |  |
| `headVersion.name` | string | File or Folder Name |
| `headVersion.parentId` | string | Parent Folder or Version Stack ID |
| `headVersion.project` | object | Frame.io Project |
| `headVersion.project.createdAt` | date | Created Timestamp |
| `headVersion.project.description` | string | Project Description |
| `headVersion.project.id` | string | Project ID |
| `headVersion.project.name` | string | Project Name |
| `headVersion.project.owner` | object | User details |
| `headVersion.project.owner.active` | boolean | User active status |
| `headVersion.project.owner.adobeUserId` | string | Adobe user ID |
| `headVersion.project.owner.avatarUrl` | string | User avatar image url |
| `headVersion.project.owner.email` | string | User email |
| `headVersion.project.owner.id` | string | User ID - can be null for invited users with no frame account |
| `headVersion.project.owner.name` | string | User name |
| `headVersion.project.restricted` | boolean | Whether the project is restricted or not |
| `headVersion.project.rootFolderId` | string | Root Folder ID |
| `headVersion.project.status` | string | Project Status |
| `headVersion.project.storage` | number | Storage Usage |
| `headVersion.project.updatedAt` | date | Updated Timestamp |
| `headVersion.project.viewUrl` | string | URL to view the project in the Frame.io web application |
| `headVersion.project.workspaceId` | string | Workspace ID |
| `headVersion.projectId` | string | Project ID |
| `headVersion.status` | string |  |
| `headVersion.type` | string |  |
| `headVersion.updatedAt` | date | Update timestamp |
| `headVersion.viewUrl` | string | URL to view the asset in the Frame.io web application |
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

Through the native Frame.io v4 API, this operation is `GET /accounts/:accountId/version_stacks/:versionStackId` (base URL `https://api.frame.io/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-version-stack.md) for the provider-specific parameters and requirements.

