# Microsoft SharePoint Online: Get Drive Item

Retrieves a drive item from Microsoft SharePoint Online.

```
GET https://connect.mindcloud.co/v1/universal/microsoftSharePointOnline/latest/actions/get-drive-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft SharePoint Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftSharePointOnline/latest/actions/get-drive-item?connectionId=$CONNECTION_ID&driveId=driveId&itemId=itemId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "driveId": "driveId",
  "itemId": "itemId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftSharePointOnline/latest/actions/get-drive-item?${params}`, {
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
| `driveId` | string | yes | Microsoft Graph drive ID for the SharePoint document library. Example: `driveId`. |
| `itemId` | string | yes | Microsoft Graph drive item ID. Example: `itemId`. |

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

Through the native Microsoft SharePoint Online API, this operation is `GET /v1.0/drives/{{driveId}}/items/{{itemId}}` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-drive-item.md) for the provider-specific parameters and requirements.

