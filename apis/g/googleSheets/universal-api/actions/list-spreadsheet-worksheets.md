# Google Sheets: List Spreadsheet Worksheets

Retrieves worksheets from a Google Sheets spreadsheet.

```
GET https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/list-spreadsheet-worksheets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Sheets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/list-spreadsheet-worksheets?connectionId=$CONNECTION_ID&spreadsheetId=Select%20a%20spreadsheet%2C%20or%20click%20%7B%7D%20to%20paste%20a%20spreadsheet%20ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spreadsheetId": "Select a spreadsheet, or click {} to paste a spreadsheet ID"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/list-spreadsheet-worksheets?${params}`, {
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
| `spreadsheetId` | string<string> | yes | Select a spreadsheet from the list. If you do not see the spreadsheet, click {} and paste the spreadsheet ID from a List Spreadsheets step or directly from the Google Sheets URL. Example: `Select a spreadsheet, or click {} to paste a spreadsheet ID`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "gridProperties": {
        "columnCount": 1,
        "rowCount": 1
      },
      "index": 1,
      "sheetId": 1,
      "sheetType": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gridProperties.columnCount` | number |  |
| `gridProperties.rowCount` | number |  |
| `index` | number |  |
| `sheetId` | number |  |
| `sheetType` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Google Sheets API, this operation is `GET spreadsheets/:spreadsheetId?fields=sheets.properties` (base URL `https://sheets.googleapis.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-spreadsheet-worksheets.md) for the provider-specific parameters and requirements.

