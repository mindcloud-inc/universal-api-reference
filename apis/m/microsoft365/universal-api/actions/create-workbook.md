# Microsoft 365: Create Workbook

Creates a workbook in Microsoft 365.

```
POST https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/create-workbook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/create-workbook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/create-workbook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Excel workbook file name including the .xlsx extension. |

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
        "context": "string",
        "etag": "string"
      },
      "commentSettings": {
        "commentingDisabled": {
          "isDisabled": true
        }
      },
      "createdBy": {
        "application": {
          "displayName": "Ava Chen",
          "id": "string"
        },
        "user": {
          "displayName": "Ava Chen",
          "email": "ava@example.com"
        }
      },
      "createdDateTime": "string",
      "cTag": "string",
      "eTag": "string",
      "file": {
        "hashes": {
          "quickXorHash": "string"
        },
        "mimeType": "string"
      },
      "fileSystemInfo": {
        "createdDateTime": "string",
        "lastModifiedDateTime": "string"
      },
      "id": "string",
      "lastModifiedBy": {
        "application": {
          "displayName": "Ava Chen",
          "id": "string"
        },
        "user": {
          "displayName": "Ava Chen",
          "email": "ava@example.com"
        }
      },
      "lastModifiedDateTime": "string",
      "name": "Ava Chen",
      "parentReference": {
        "driveId": "string",
        "driveType": "string",
        "id": "string",
        "path": "string",
        "sharepointIds": {
          "listId": "string",
          "listItemUniqueId": "string",
          "siteId": "string",
          "siteUrl": "https://example.com",
          "tenantId": "string",
          "webId": "string"
        }
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
| `@odata.etag` | string |  |
| `commentSettings.commentingDisabled.isDisabled` | boolean |  |
| `createdBy.application.displayName` | string |  |
| `createdBy.application.id` | string |  |
| `createdBy.user.displayName` | string |  |
| `createdBy.user.email` | string |  |
| `createdDateTime` | string |  |
| `cTag` | string |  |
| `eTag` | string |  |
| `file.hashes.quickXorHash` | string |  |
| `file.mimeType` | string |  |
| `fileSystemInfo.createdDateTime` | string |  |
| `fileSystemInfo.lastModifiedDateTime` | string |  |
| `id` | string |  |
| `lastModifiedBy.application.displayName` | string |  |
| `lastModifiedBy.application.id` | string |  |
| `lastModifiedBy.user.displayName` | string |  |
| `lastModifiedBy.user.email` | string |  |
| `lastModifiedDateTime` | string |  |
| `name` | string |  |
| `parentReference.driveId` | string |  |
| `parentReference.driveType` | string |  |
| `parentReference.id` | string |  |
| `parentReference.path` | string |  |
| `parentReference.sharepointIds.listId` | string |  |
| `parentReference.sharepointIds.listItemUniqueId` | string |  |
| `parentReference.sharepointIds.siteId` | string |  |
| `parentReference.sharepointIds.siteUrl` | string |  |
| `parentReference.sharepointIds.tenantId` | string |  |
| `parentReference.sharepointIds.webId` | string |  |
| `size` | number |  |
| `webUrl` | string |  |

## Native endpoint

Through the native Microsoft 365 API, this operation is `POST /v1.0/me/drive/root/children` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workbook.md) for the provider-specific parameters and requirements.

