# Microsoft 365 Excel: Create Table

Creates a table in a Microsoft 365 Excel worksheet.

```
POST https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/create-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Excel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/create-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "driveItemId": "string",
  "worksheetName": "RuntimeVerify",
  "address": "A1:B2",
  "hasHeaders": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/create-table', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "driveItemId": "string",
    "worksheetName": "RuntimeVerify",
    "address": "A1:B2",
    "hasHeaders": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `driveItemId` | string | yes |  |
| `worksheetName` | string | yes | Example: `RuntimeVerify`. |
| `address` | string | yes | The range address to convert into a table, for example RuntimeVerify!A1:B2. Example: `A1:B2`. |
| `hasHeaders` | boolean | yes | Default: `true`. |

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
| `id` | string |  |
| `name` | string |  |
| `showHeaders` | boolean |  |
| `showTotals` | boolean |  |
| `style` | string |  |

## Native endpoint

Through the native Microsoft 365 Excel API, this operation is `POST /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/tables/add` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-table.md) for the provider-specific parameters and requirements.

