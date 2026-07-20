# Google Sheets: List Spreadsheet Columns

Retrieves columns from a Google Sheets worksheet.

```
GET https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/list-spreadsheet-columns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Sheets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/list-spreadsheet-columns?connectionId=$CONNECTION_ID&spreadsheetId=Select%20a%20spreadsheet%2C%20or%20click%20%7B%7D%20to%20paste%20a%20spreadsheet%20ID&worksheet=Select%20a%20worksheet%2C%20or%20click%20%7B%7D%20to%20enter%20the%20worksheet%20name&columns=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spreadsheetId": "Select a spreadsheet, or click {} to paste a spreadsheet ID",
  "worksheet": "Select a worksheet, or click {} to enter the worksheet name",
  "columns": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/list-spreadsheet-columns?${params}`, {
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
| `spreadsheetId` | list<list> | yes | Select a spreadsheet from the list. If you do not see the spreadsheet, click {} and paste the spreadsheet ID from a List Spreadsheets step or directly from the Google Sheets URL. Example: `Select a spreadsheet, or click {} to paste a spreadsheet ID`. |
| `worksheet` | list<string> | yes | Select a worksheet from the list. If you do not see it, click {} and enter the worksheet tab name. You can get the exact name from a List Spreadsheet Worksheets step. Use the worksheet name, not the worksheet ID. Example: `Select a worksheet, or click {} to enter the worksheet name`. |
| `columns` | string<string> | yes | Columns to fetch - A - A1 |
| `end` | number | no |  |
| `start` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "majorDimension": "string",
      "range": "string",
      "values": [
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
| `majorDimension` | string |  |
| `range` | string |  |
| `values[]` | object |  |

## Native endpoint

Through the native Google Sheets API, this operation is `GET spreadsheets/:spreadsheetId/values:method` (base URL `https://sheets.googleapis.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-spreadsheet-columns.md) for the provider-specific parameters and requirements.

