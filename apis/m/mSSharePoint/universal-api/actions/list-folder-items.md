# MS SharePoint: List Folder Items

Retrieves items from a SharePoint folder.

```
GET https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/list-folder-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MS SharePoint `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/list-folder-items?connectionId=$CONNECTION_ID&limit=25&offset=0&driveId=string&folderPath=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "driveId": "string",
  "folderPath": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/list-folder-items?${params}`, {
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
| `driveId` | string | yes | Microsoft Graph drive ID. |
| `folderPath` | string | yes | Folder path relative to the drive root. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": {},
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "file": {},
      "folder": {},
      "id": "string",
      "lastModifiedBy": {},
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "parentReference": {},
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
| `createdBy` | object |  |
| `createdDateTime` | date |  |
| `file` | object |  |
| `folder` | object |  |
| `id` | string |  |
| `lastModifiedBy` | object |  |
| `lastModifiedDateTime` | date |  |
| `name` | string |  |
| `parentReference` | object |  |
| `size` | number |  |
| `webUrl` | string |  |

## Native endpoint

Through the native MS SharePoint API, this operation is `GET /v1.0/drives/{{driveId}}/root:/{{folderPath}}:/children` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-folder-items.md) for the provider-specific parameters and requirements.

