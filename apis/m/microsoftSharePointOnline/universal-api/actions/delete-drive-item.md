# Microsoft SharePoint Online: Delete Drive Item

Deletes a drive item from Microsoft SharePoint Online.

```
DELETE https://connect.mindcloud.co/v1/universal/microsoftSharePointOnline/latest/actions/delete-drive-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft SharePoint Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/microsoftSharePointOnline/latest/actions/delete-drive-item?connectionId=$CONNECTION_ID&driveId=driveId&itemId=itemId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "driveId": "driveId",
  "itemId": "itemId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftSharePointOnline/latest/actions/delete-drive-item?${params}`, {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft SharePoint Online API returns.

## Native endpoint

Through the native Microsoft SharePoint Online API, this operation is `DELETE /v1.0/drives/{{driveId}}/items/{{itemId}}` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-drive-item.md) for the provider-specific parameters and requirements.

