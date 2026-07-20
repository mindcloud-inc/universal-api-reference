# Google Sheets Universal API Examples

These examples use the MindCloud API key and Google Sheets connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Spreadsheet Metadata

Retrieves spreadsheet metadata from Google Sheets.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/get-spreadsheet-metadata?connectionId=$CONNECTION_ID&spreadsheetId=Select%20a%20spreadsheet%2C%20or%20click%20%7B%7D%20to%20paste%20a%20spreadsheet%20ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spreadsheetId": "Select a spreadsheet, or click {} to paste a spreadsheet ID"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/get-spreadsheet-metadata?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Get Spreadsheet Metadata action reference](actions/get-spreadsheet-metadata.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleSheets/latest/actions/get-spreadsheet-metadata).

## Append Rows

Appends rows to a Google Sheets worksheet.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/append-rows" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spreadsheetId": "Select a spreadsheet, or click {} to paste a spreadsheet ID",
  "worksheet": "Select a worksheet, or click {} to enter the worksheet name",
  "values[]": [
    [
      "string"
    ]
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/append-rows', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spreadsheetId": "Select a spreadsheet, or click {} to paste a spreadsheet ID",
    "worksheet": "Select a worksheet, or click {} to enter the worksheet name",
    "values[]": [["string"]]
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "spreadsheetId": "string",
      "tableRange": "string",
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

See the full [Append Rows action reference](actions/append-rows.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleSheets/latest/actions/append-rows).
