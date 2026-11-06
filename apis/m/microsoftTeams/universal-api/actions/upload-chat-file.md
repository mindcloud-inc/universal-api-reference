# Microsoft Teams: Upload Chat File



```
POST https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/upload-chat-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Teams `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/upload-chat-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileName": "report.pdf",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/upload-chat-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `fileName` | string | yes | File name including extension. Saves in the connected user's OneDrive root. An existing file with the same name is replaced; use a unique name to avoid replacing another file. Example: `report.pdf`. |
| `content` | file | yes | Base64 file content or a direct HTTPS download URL. Uploads binary bytes using the Teams connection. Does not share the file or send a message. |

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
| `size` | number |  |
| `webUrl` | string |  |

## Native endpoint

Through the native Microsoft Teams API, this operation is `PUT /v1.0/me/drive/root:/:fileName:/content` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-chat-file.md) for the provider-specific parameters and requirements.

