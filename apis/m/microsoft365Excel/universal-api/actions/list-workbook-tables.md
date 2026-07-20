# Microsoft 365 Excel: List Workbook Tables

Retrieves tables from a Microsoft 365 Excel workbook.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/list-workbook-tables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Excel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/list-workbook-tables?connectionId=$CONNECTION_ID&siteId=string&driveItemId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteId": "string",
  "driveItemId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/list-workbook-tables?${params}`, {
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
| `siteId` | string | yes | SharePoint site ID for the workbook file. |
| `driveItemId` | string | yes | Drive item ID of the Excel workbook file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "showHeaders": true,
      "showTotals": true,
      "style": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Workbook table ID. |
| `name` | string | Workbook table name. |
| `showHeaders` | boolean | Whether the table displays header rows. |
| `showTotals` | boolean | Whether the table displays a totals row. |
| `style` | string | Workbook table style name. |

## Native endpoint

Through the native Microsoft 365 Excel API, this operation is `GET /v1.0/sites/:siteId/drive/items/:driveItemId/workbook/tables` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workbook-tables.md) for the provider-specific parameters and requirements.

