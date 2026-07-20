# Google Sheets: Clear Row

Clears row contents in Google Sheets while keeping rows intact.

```
DELETE https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/clear-row
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Sheets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/clear-row?connectionId=$CONNECTION_ID&spreadsheetId=Select%20a%20spreadsheet%2C%20or%20click%20%7B%7D%20to%20paste%20a%20spreadsheet%20ID&worksheet=Select%20a%20worksheet%2C%20or%20click%20%7B%7D%20to%20enter%20the%20worksheet%20name&rows=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spreadsheetId": "Select a spreadsheet, or click {} to paste a spreadsheet ID",
  "worksheet": "Select a worksheet, or click {} to enter the worksheet name",
  "rows": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/clear-row?${params}`, {
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
| `spreadsheetId` | list | yes | Select a spreadsheet from the list. If you do not see the spreadsheet, click {} and paste the spreadsheet ID from a List Spreadsheets step or directly from the Google Sheets URL. Example: `Select a spreadsheet, or click {} to paste a spreadsheet ID`. |
| `worksheet` | list<string> | yes | Select a worksheet from the list. If you do not see it, click {} and enter the worksheet tab name. You can get the exact name from a List Spreadsheet Worksheets step. Use the worksheet name, not the worksheet ID. Example: `Select a worksheet, or click {} to enter the worksheet name`. |
| `rows` | string | yes | Rows remain intact, only their contents will be cleared. Accepts: - Individual row numbers (e.g. 3) - Ranges (e.g. 3–5) - Comma-separated lists (e.g. 3, 4, 6) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clearedRanges": [
        "string"
      ],
      "spreadsheetId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clearedRanges[]` | string |  |
| `spreadsheetId` | string |  |

## Native endpoint

Through the native Google Sheets API, this operation is `POST spreadsheets/:spreadsheetId/values:method` (base URL `https://sheets.googleapis.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clear-row.md) for the provider-specific parameters and requirements.

