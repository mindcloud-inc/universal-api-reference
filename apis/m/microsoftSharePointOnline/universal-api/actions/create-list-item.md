# Microsoft SharePoint Online: Create List Item

Creates a list item in Microsoft SharePoint Online.

```
POST https://connect.mindcloud.co/v1/universal/microsoftSharePointOnline/latest/actions/create-list-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft SharePoint Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftSharePointOnline/latest/actions/create-list-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteId": "contoso.sharepoint.com,siteCollectionId,siteId",
  "listId": "Documents",
  "fields": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftSharePointOnline/latest/actions/create-list-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "siteId": "contoso.sharepoint.com,siteCollectionId,siteId",
    "listId": "Documents",
    "fields": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteId` | string | yes | Microsoft Graph site ID for the SharePoint site. Example: `contoso.sharepoint.com,siteCollectionId,siteId`. |
| `listId` | string | yes | Microsoft Graph list ID or list name for the SharePoint list. Example: `Documents`. |
| `fields` | object | yes | Object containing SharePoint list column values for the new item. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": {},
      "createdBy": {},
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "fields": {},
      "id": "string",
      "lastModifiedBy": {},
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "parentReference": {},
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | object |  |
| `createdBy` | object |  |
| `createdDateTime` | date |  |
| `fields` | object |  |
| `id` | string |  |
| `lastModifiedBy` | object |  |
| `lastModifiedDateTime` | date |  |
| `parentReference` | object |  |
| `webUrl` | string |  |

## Native endpoint

Through the native Microsoft SharePoint Online API, this operation is `POST /v1.0/sites/{{siteId}}/lists/{{listId}}/items` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-list-item.md) for the provider-specific parameters and requirements.

