# MS SharePoint: Get List Item Fields

Retrieves field values for a SharePoint list item.

```
GET https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/get-list-item-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MS SharePoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/get-list-item-fields?connectionId=$CONNECTION_ID&siteId=string&listId=string&itemId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteId": "string",
  "listId": "string",
  "itemId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/get-list-item-fields?${params}`, {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MS SharePoint API returns.

## Native endpoint

Through the native MS SharePoint API, this operation is `GET /v1.0/sites/{{siteId}}/lists/{{listId}}/items/{{itemId}}/fields` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list-item-fields.md) for the provider-specific parameters and requirements.

