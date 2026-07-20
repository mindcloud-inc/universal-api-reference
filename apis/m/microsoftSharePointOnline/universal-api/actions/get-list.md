# Microsoft SharePoint Online: Get List

Retrieves a list from Microsoft SharePoint Online.

```
GET https://connect.mindcloud.co/v1/universal/microsoftSharePointOnline/latest/actions/get-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft SharePoint Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftSharePointOnline/latest/actions/get-list?connectionId=$CONNECTION_ID&siteId=contoso.sharepoint.com%2CsiteCollectionId%2CsiteId&listId=Documents" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteId": "contoso.sharepoint.com,siteCollectionId,siteId",
  "listId": "Documents"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftSharePointOnline/latest/actions/get-list?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": {},
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "displayName": "Ava Chen",
      "eTag": "string",
      "id": "string",
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "list": {},
      "name": "Ava Chen",
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
| `createdBy` | object |  |
| `createdDateTime` | date |  |
| `description` | string |  |
| `displayName` | string |  |
| `eTag` | string |  |
| `id` | string |  |
| `lastModifiedDateTime` | date |  |
| `list` | object |  |
| `name` | string |  |
| `parentReference` | object |  |
| `webUrl` | string |  |

## Native endpoint

Through the native Microsoft SharePoint Online API, this operation is `GET /v1.0/sites/{{siteId}}/lists/{{listId}}` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list.md) for the provider-specific parameters and requirements.

