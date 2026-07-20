# Frame.io v4: Get File

Retrieves a file from Frame.io v4.

```
GET https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/get-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frame.io v4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/get-file?connectionId=$CONNECTION_ID&accountId=string&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/get-file?${params}`, {
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
| `fileId` | string | yes |  |
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
| `fileSize` | number | File size in bytes |
| `id` | string | File, Folder, or Version Stack ID |
| `mediaLinks` | object |  |
| `mediaLinks.efficient` | object |  |
| `mediaLinks.efficient.downloadUrl` | string | URL to download the media file.<br/> HTTP response headers will include Content-Disposition = 'attachment;filename=<filename>'.<br/> Watermarks may be applied for transcode links as per Account settings and User permissions.<br/> |
| `mediaLinks.highQuality` | object |  |
| `mediaLinks.highQuality.downloadUrl` | string | URL to download the media file.<br/> HTTP response headers will include Content-Disposition = 'attachment;filename=<filename>'.<br/> Watermarks may be applied for transcode links as per Account settings and User permissions.<br/> |
| `mediaLinks.original` | object |  |
| `mediaLinks.original.downloadUrl` | string | URL to download the media file.<br/> HTTP response headers will include Content-Disposition = 'attachment;filename=<filename>'.<br/> Watermarks may be applied for transcode links as per Account settings and User permissions.<br/> |
| `mediaLinks.original.inlineUrl` | string | URL to view the media file in a web browser in its original resolution and media type.<br/> HTTP response headers will include Content-Disposition = 'inline;filename=<filename>'.<br/> |
| `mediaLinks.scrubSheet` | object |  |
| `mediaLinks.scrubSheet.downloadUrl` | string | URL to download the media file.<br/> HTTP response headers will include Content-Disposition = 'attachment;filename=<filename>'.<br/> Watermarks may be applied for transcode links as per Account settings and User permissions.<br/> |
| `mediaLinks.scrubSheet.url` | string | URL to transcoded media that won't include any Content-Disposition header in the response.<br/> Watermarks may be applied as per Account settings and User permissions.<br/> Media content may be streamed (e.g. when watermarks are required). Clients may issue a HEAD request to determine whether Content-Length and/or Accept-Ranges headers are present in order to determine whether the content can be downloaded in parallel chunks. |
| `mediaLinks.thumbnail` | object |  |
| `mediaLinks.thumbnail.downloadUrl` | string | URL to download the media file.<br/> HTTP response headers will include Content-Disposition = 'attachment;filename=<filename>'.<br/> Watermarks may be applied for transcode links as per Account settings and User permissions.<br/> |
| `mediaLinks.thumbnail.url` | string | URL to transcoded media that won't include any Content-Disposition header in the response.<br/> Watermarks may be applied as per Account settings and User permissions.<br/> Media content may be streamed (e.g. when watermarks are required). Clients may issue a HEAD request to determine whether Content-Length and/or Accept-Ranges headers are present in order to determine whether the content can be downloaded in parallel chunks. |
| `mediaLinks.thumbnailHighQuality` | object |  |
| `mediaLinks.thumbnailHighQuality.downloadUrl` | string | URL to download the media file.<br/> HTTP response headers will include Content-Disposition = 'attachment;filename=<filename>'.<br/> Watermarks may be applied for transcode links as per Account settings and User permissions.<br/> |
| `mediaLinks.thumbnailHighQuality.url` | string | URL to transcoded media that won't include any Content-Disposition header in the response.<br/> Watermarks may be applied as per Account settings and User permissions.<br/> Media content may be streamed (e.g. when watermarks are required). Clients may issue a HEAD request to determine whether Content-Length and/or Accept-Ranges headers are present in order to determine whether the content can be downloaded in parallel chunks. |
| `mediaLinks.videoH264180` | object |  |
| `mediaLinks.videoH264180.downloadUrl` | string | URL to download the media file.<br/> HTTP response headers will include Content-Disposition = 'attachment;filename=<filename>'.<br/> Watermarks may be applied for transcode links as per Account settings and User permissions.<br/> |
| `mediaLinks.videoH264180.url` | string | URL to transcoded media that won't include any Content-Disposition header in the response.<br/> Watermarks may be applied as per Account settings and User permissions.<br/> Media content may be streamed (e.g. when watermarks are required). Clients may issue a HEAD request to determine whether Content-Length and/or Accept-Ranges headers are present in order to determine whether the content can be downloaded in parallel chunks. |
| `mediaType` | string | File media type |
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
| `status` | string |  |
| `type` | string |  |
| `updatedAt` | date | Update timestamp |
| `viewUrl` | string | URL to view the asset in the Frame.io web application |

## Native endpoint

Through the native Frame.io v4 API, this operation is `GET /accounts/:accountId/files/:fileId` (base URL `https://api.frame.io/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file.md) for the provider-specific parameters and requirements.

