# MS SharePoint: Get List Item

Retrieves a SharePoint list item.

```
GET https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/get-list-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MS SharePoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/get-list-item?connectionId=$CONNECTION_ID&siteId=string&listId=string&itemId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteId": "string",
  "listId": "string",
  "itemId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/get-list-item?${params}`, {
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
| `siteId` | string | yes | Microsoft Graph SharePoint site ID. |
| `listId` | string | yes | SharePoint list ID. |
| `itemId` | string | yes | SharePoint list item ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": {},
      "createdBy": {},
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "eTag": "string",
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
| `eTag` | string |  |
| `fields` | object |  |
| `id` | string |  |
| `lastModifiedBy` | object |  |
| `lastModifiedDateTime` | date |  |
| `parentReference` | object |  |
| `webUrl` | string |  |

## Native endpoint

Through the native MS SharePoint API, this operation is `GET /v1.0/sites/{{siteId}}/lists/{{listId}}/items/{{itemId}}` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list-item.md) for the provider-specific parameters and requirements.

