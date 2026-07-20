# Microsoft SharePoint Online: Get List Item

Retrieves a list item from Microsoft SharePoint Online.

```
GET https://connect.mindcloud.co/v1/universal/microsoftSharePointOnline/latest/actions/get-list-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft SharePoint Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftSharePointOnline/latest/actions/get-list-item?connectionId=$CONNECTION_ID&siteId=contoso.sharepoint.com%2CsiteCollectionId%2CsiteId&listId=Documents&itemId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteId": "contoso.sharepoint.com,siteCollectionId,siteId",
  "listId": "Documents",
  "itemId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftSharePointOnline/latest/actions/get-list-item?${params}`, {
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
| `siteId` | string | yes | Microsoft Graph site ID for the SharePoint site. Example: `contoso.sharepoint.com,siteCollectionId,siteId`. |
| `listId` | string | yes | Microsoft Graph list ID or list name for the SharePoint list. Example: `Documents`. |
| `itemId` | string | yes | Microsoft Graph list item ID. Example: `1`. |

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

Through the native Microsoft SharePoint Online API, this operation is `GET /v1.0/sites/{{siteId}}/lists/{{listId}}/items/{{itemId}}` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list-item.md) for the provider-specific parameters and requirements.

