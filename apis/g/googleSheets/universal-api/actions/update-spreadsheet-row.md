# Google Sheets: Update Spreadsheet Row

Updates a row in a Google Sheets worksheet.

```
PUT https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/update-spreadsheet-row
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Sheets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/update-spreadsheet-row" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spreadsheetId": "Select a spreadsheet, or click {} to paste a spreadsheet ID",
  "worksheet": "Select a worksheet, or click {} to enter the worksheet name"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/update-spreadsheet-row', {
  method: 'PUT',
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
| `values` | object<string> | no |  |
| `worksheet` | list<list> | yes | Select a worksheet from the list. If you do not see it, click {} and enter the worksheet tab name. You can get the exact name from a List Spreadsheet Worksheets step. Use the worksheet name, not the worksheet ID. Example: `Select a worksheet, or click {} to enter the worksheet name`. |
| `row` | string<string> | no | The row number to update. Note: row 1 typically contains the spreadsheet headers, so you may want to avoid modifying it. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Sheets API returns.

## Native endpoint

Through the native Google Sheets API, this operation is `PUT spreadsheets/:spreadsheetId/values/:worksheet!:row::row` (base URL `https://sheets.googleapis.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-spreadsheet-row.md) for the provider-specific parameters and requirements.

