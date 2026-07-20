# Microsoft 365 Excel: Update Range Values

Updates worksheet range values in Microsoft 365 Excel.

```
PUT https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/update-range-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Excel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/update-range-values" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "driveItemId": "string",
  "worksheetName": "Ava Chen",
  "startCell": "A1",
  "endCell": "B3",
  "values": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/update-range-values', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "driveItemId": "string",
    "worksheetName": "Ava Chen",
    "startCell": "A1",
    "endCell": "B3",
    "values": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `driveItemId` | string | yes | Drive item ID of the Excel workbook file. |
| `worksheetName` | string | yes | Worksheet name exactly as it appears in the workbook, such as Sheet1 or Summary. |
| `startCell` | string | yes | Top-left cell in the target range, such as A1. Example: `A1`. |
| `endCell` | string | yes | Bottom-right cell in the target range, such as B3. Example: `B3`. |
| `values` | object | yes | Two-dimensional JSON array of cell values to write into the target range. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@odata": {
        "context": "string",
        "id": "string"
      },
      "address": "string",
      "addressLocal": "string",
      "cellCount": 1,
      "columnCount": 1,
      "columnHidden": true,
      "columnIndex": 1,
      "formulas": [
        {}
      ],
      "formulasLocal": [
        {}
      ],
      "formulasR1C1": [
        {}
      ],
      "hidden": true,
      "numberFormat": [
        {}
      ],
      "rowCount": 1,
      "rowHidden": true,
      "rowIndex": 1,
      "text": [
        {}
      ],
      "values": [
        {}
      ],
      "valueTypes": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@odata.context` | string |  |
| `@odata.id` | string |  |
| `address` | string |  |
| `addressLocal` | string |  |
| `cellCount` | number |  |
| `columnCount` | number |  |
| `columnHidden` | boolean |  |
| `columnIndex` | number |  |
| `formulas[]` | object |  |
| `formulasLocal[]` | object |  |
| `formulasR1C1[]` | object |  |
| `hidden` | boolean |  |
| `numberFormat[]` | object |  |
| `rowCount` | number |  |
| `rowHidden` | boolean |  |
| `rowIndex` | number |  |
| `text[]` | object |  |
| `values[]` | object |  |
| `valueTypes[]` | object |  |

## Native endpoint

Through the native Microsoft 365 Excel API, this operation is `PATCH /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/range(address='{{startCell}}\:{{endCell}}')` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-range-values.md) for the provider-specific parameters and requirements.

