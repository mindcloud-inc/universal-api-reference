# Google Sheets Universal API Examples

These examples use the MindCloud API key and Google Sheets connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Spreadsheets

Retrieves accessible Google Sheets files from Google Drive.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/list-spreadsheets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/list-spreadsheets?${params}`, {
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
  "data": [
    {
      "createdTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Spreadsheets action reference](actions/list-spreadsheets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleSheets/latest/actions/list-spreadsheets).

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
