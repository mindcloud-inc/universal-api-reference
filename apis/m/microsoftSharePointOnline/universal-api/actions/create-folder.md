# Microsoft SharePoint Online: Create Folder

Creates a folder in Microsoft SharePoint Online.

```
POST https://connect.mindcloud.co/v1/universal/microsoftSharePointOnline/latest/actions/create-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft SharePoint Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftSharePointOnline/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "driveId": "driveId",
  "name": "Invoices"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftSharePointOnline/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "driveId": "driveId",
    "name": "Invoices"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `driveId` | string | yes | Microsoft Graph drive ID for the SharePoint document library. Example: `driveId`. |
| `name` | string | yes | Name of the folder to create. Example: `Invoices`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": {},
      "createdDateTime": "2026-05-07T12:00:00.000Z",
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
| `folder` | object |  |
| `id` | string |  |
| `lastModifiedBy` | object |  |
| `lastModifiedDateTime` | date |  |
| `name` | string |  |
| `parentReference` | object |  |
| `size` | number |  |
| `webUrl` | string |  |

## Native endpoint

Through the native Microsoft SharePoint Online API, this operation is `POST /v1.0/drives/{{driveId}}/root/children` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-folder.md) for the provider-specific parameters and requirements.

