# Zoho Sheet: Create Table

Creates a new table in Zoho Sheet.

```
POST https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/create-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/create-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resourceId": "string",
  "worksheetName": "Ava Chen",
  "startRow": 1,
  "startColumn": 1,
  "endRow": 1,
  "endColumn": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/create-table', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resourceId": "string",
    "worksheetName": "Ava Chen",
    "startRow": 1,
    "startColumn": 1,
    "endRow": 1,
    "endColumn": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resourceId` | string | yes | The workbook resource ID. |
| `worksheetName` | string | yes | Name of the worksheet |
| `startRow` | number | yes | start row index of the table |
| `startColumn` | number | yes | start column index of the table |
| `endRow` | number | yes | end row index of the table |
| `endColumn` | number | yes | end column index of the table |
| `containsHeader` | boolean | no | Optional parameter. The default value is true. If set to false, the header row will be inserted at the top as an additional row to the selected range. |
| `headerNames` | string | no | Optional parameter. Array of header values for the created table. The header_names must be unique. For example : ["country","region"]. The length of header_names and column length of the table must be equal. Provide this value as a valid JSON string. |
| `tableStyle` | string | no | Optional parameter. A json array of styles and properties for table. The template and color values correspond to the options provided in the spreadsheet. Instead of the predefined color options (Accent1 to Accent6), hex color codes can also be used. Example: {"template":"light1", "color":"#FF5733", "properties" : {"first_column":true, "last_column":true, "banded_rows":true, "banded_columns":false, "total_row":false}}. The default table_styles for a table is {"template":"Medium1", "color":"Accent1", "properties": {"first_column":false, "last_column":false, "banded_rows":true, "banded_columns":false, "total_row":false}} Provide this value as a valid JSON string. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `worksheetId` | string | no | Alternatively worksheet_id can be used instead of worksheet_name |

## Response

```json
{
  "success": true,
  "data": [
    {
      "method": "string",
      "status": "string",
      "tableId": 1,
      "tableName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `method` | string |  |
| `status` | string |  |
| `tableId` | number |  |
| `tableName` | string |  |

## Native endpoint

Through the native Zoho Sheet API, this operation is `POST /:resourceId` (base URL `https://sheet.zoho.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-table.md) for the provider-specific parameters and requirements.

