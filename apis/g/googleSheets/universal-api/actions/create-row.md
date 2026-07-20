# Google Sheets: Create Row

Creates a new row in a Google Sheets worksheet.

```
POST https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/create-row
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Sheets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/create-row" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spreadsheetId": "Select a spreadsheet, or click {} to paste a spreadsheet ID",
  "worksheet": "Select a worksheet, or click {} to enter the worksheet name"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/create-row', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spreadsheetId": "Select a spreadsheet, or click {} to paste a spreadsheet ID",
    "worksheet": "Select a worksheet, or click {} to enter the worksheet name"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `spreadsheetId` | list<list> | yes | Select a spreadsheet from the list. If you do not see the spreadsheet, click {} and paste the spreadsheet ID from a List Spreadsheets step or directly from the Google Sheets URL. Example: `Select a spreadsheet, or click {} to paste a spreadsheet ID`. |
| `values` | object<array> | no |  |
| `worksheet` | list<string> | yes | Select a worksheet from the list. If you do not see it, click {} and enter the worksheet tab name. You can get the exact name from a List Spreadsheet Worksheets step. Use the worksheet name, not the worksheet ID. Example: `Select a worksheet, or click {} to enter the worksheet name`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "spreadsheetId": "string",
      "updates": {
        "spreadsheetId": "string",
        "updatedCells": 1,
        "updatedColumns": 1,
        "updatedRange": "string",
        "updatedRows": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `spreadsheetId` | string |  |
| `updates.spreadsheetId` | string |  |
| `updates.updatedCells` | number |  |
| `updates.updatedColumns` | number |  |
| `updates.updatedRange` | string |  |
| `updates.updatedRows` | number |  |

## Native endpoint

Through the native Google Sheets API, this operation is `POST spreadsheets/:spreadsheetId/values/:worksheet!:range:append` (base URL `https://sheets.googleapis.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-row.md) for the provider-specific parameters and requirements.

