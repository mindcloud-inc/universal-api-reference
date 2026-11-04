# Microsoft Teams: Upload Channel File



```
POST https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/upload-channel-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Teams `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/upload-channel-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "driveId": "string",
  "folderId": "string",
  "fileName": "report.pdf",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/upload-channel-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "driveId": "string",
    "folderId": "string",
    "fileName": "report.pdf",
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `driveId` | string | yes | Use parentReference.driveId returned by Get Channel Files Folder. |
| `folderId` | string | yes | Use id returned by Get Channel Files Folder. Do not use the channel ID. |
| `fileName` | string | yes | Destination file name, including extension. An existing file with this name is replaced. Example: `report.pdf`. |
| `content` | file | yes | Base64 file content or a direct HTTPS download URL. The file is uploaded as binary bytes using this Teams connection. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@microsoft": {
        "graph": {
          "downloadUrl": "https://example.com"
        }
      },
      "@odata": {
        "context": "string"
      },
      "createdBy": {
        "application": {
          "displayName": "Ava Chen",
          "id": "string"
        },
        "user": {
          "displayName": "Ava Chen",
          "email": "ava@example.com",
          "id": "string"
        }
      },
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "cTag": "string",
      "eTag": "string",
      "file": {
        "hashes": {
          "quickXorHash": "string"
        },
        "mimeType": "string"
      },
      "fileSystemInfo": {
        "createdDateTime": "2026-05-07T12:00:00.000Z",
        "lastModifiedDateTime": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "isAuthoritative": true,
      "lastModifiedBy": {
        "application": {
          "displayName": "Ava Chen",
          "id": "string"
        },
        "user": {
          "displayName": "Ava Chen",
          "email": "ava@example.com",
          "id": "string"
        }
      },
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "parentReference": {
        "driveId": "string",
        "driveType": "string",
        "id": "string",
        "name": "Ava Chen",
        "path": "string",
        "siteId": "string"
      },
      "shared": {
        "scope": "string"
      },
      "size": 1,
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@microsoft.graph.downloadUrl` | string |  |
| `@odata.context` | string |  |
| `createdBy` | object |  |
| `createdBy.application` | object |  |
| `createdBy.application.displayName` | string |  |
| `createdBy.application.id` | string |  |
| `createdBy.user` | object |  |
| `createdBy.user.displayName` | string |  |
| `createdBy.user.email` | string |  |
| `createdBy.user.id` | string |  |
| `createdDateTime` | date |  |
| `cTag` | string |  |
| `eTag` | string |  |
| `file` | object |  |
| `file.hashes` | object |  |
| `file.hashes.quickXorHash` | string |  |
| `file.mimeType` | string |  |
| `fileSystemInfo` | object |  |
| `fileSystemInfo.createdDateTime` | date |  |
| `fileSystemInfo.lastModifiedDateTime` | date |  |
| `id` | string |  |
| `isAuthoritative` | boolean |  |
| `lastModifiedBy` | object |  |
| `lastModifiedBy.application` | object |  |
| `lastModifiedBy.application.displayName` | string |  |
| `lastModifiedBy.application.id` | string |  |
| `lastModifiedBy.user` | object |  |
| `lastModifiedBy.user.displayName` | string |  |
| `lastModifiedBy.user.email` | string |  |
| `lastModifiedBy.user.id` | string |  |
| `lastModifiedDateTime` | date |  |
| `name` | string |  |
| `parentReference` | object |  |
| `parentReference.driveId` | string |  |
| `parentReference.driveType` | string |  |
| `parentReference.id` | string |  |
| `parentReference.name` | string |  |
| `parentReference.path` | string |  |
| `parentReference.siteId` | string |  |
| `shared` | object |  |
| `shared.scope` | string |  |
| `size` | number |  |
| `webUrl` | string |  |

## Native endpoint

Through the native Microsoft Teams API, this operation is `PUT /v1.0/drives/:driveId/items/:folderId:/:fileName:/content` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-channel-file.md) for the provider-specific parameters and requirements.

