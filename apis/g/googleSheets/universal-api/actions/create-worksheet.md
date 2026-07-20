# Google Sheets: Create Worksheet

Creates a new worksheet in Google Sheets.

```
POST https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/create-worksheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Sheets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/create-worksheet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spreadsheetId": "Select a spreadsheet, or click {} to paste a spreadsheet ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/create-worksheet', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spreadsheetId": "Select a spreadsheet, or click {} to paste a spreadsheet ID"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | no |  |
| `spreadsheetId` | list<list> | yes | Select a spreadsheet from the list. If you do not see the spreadsheet, click {} and paste the spreadsheet ID from a List Spreadsheets step or directly from the Google Sheets URL. Example: `Select a spreadsheet, or click {} to paste a spreadsheet ID`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "replies": [
        {
          "addSheet": {
            "properties": {
              "gridProperties": {
                "columnCount": 1,
                "rowCount": 1
              },
              "index": 1,
              "sheetId": 1,
              "sheetType": "string",
              "title": "string"
            }
          }
        }
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
| `replies[].addSheet.properties.gridProperties.columnCount` | number |  |
| `replies[].addSheet.properties.gridProperties.rowCount` | number |  |
| `replies[].addSheet.properties.index` | number |  |
| `replies[].addSheet.properties.sheetId` | number |  |
| `replies[].addSheet.properties.sheetType` | string |  |
| `replies[].addSheet.properties.title` | string |  |
| `spreadsheetId` | string |  |

## Native endpoint

Through the native Google Sheets API, this operation is `POST spreadsheets/:spreadsheetId:batchUpdate` (base URL `https://sheets.googleapis.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-worksheet.md) for the provider-specific parameters and requirements.

