# Google Sheets: Batch Update Spreadsheet Values

Updates explicit A1 ranges in Google Sheets.

```
PUT https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/batch-update-spreadsheet-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Sheets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/batch-update-spreadsheet-values" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spreadsheetId": "Select a spreadsheet, or click {} to paste a spreadsheet ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/batch-update-spreadsheet-values', {
  method: 'PUT',
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
| `spreadsheetId` | list<list> | yes | Select a spreadsheet from the list. If you do not see the spreadsheet, click {} and paste the spreadsheet ID from a List Spreadsheets step or directly from the Google Sheets URL. Example: `Select a spreadsheet, or click {} to paste a spreadsheet ID`. |
| `data[]` | array | no | An array of range/value objects to update in a single request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "responses": [
        {
          "spreadsheetId": "string",
          "updatedCells": 1,
          "updatedColumns": 1,
          "updatedRange": "string",
          "updatedRows": 1
        }
      ],
      "spreadsheetId": "string",
      "totalUpdatedCells": 1,
      "totalUpdatedColumns": 1,
      "totalUpdatedRows": 1,
      "totalUpdatedSheets": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `responses[].spreadsheetId` | string |  |
| `responses[].updatedCells` | number |  |
| `responses[].updatedColumns` | number |  |
| `responses[].updatedRange` | string |  |
| `responses[].updatedRows` | number |  |
| `spreadsheetId` | string |  |
| `totalUpdatedCells` | number |  |
| `totalUpdatedColumns` | number |  |
| `totalUpdatedRows` | number |  |
| `totalUpdatedSheets` | number |  |

## Native endpoint

Through the native Google Sheets API, this operation is `POST spreadsheets/:spreadsheetId/:batchUpdate` (base URL `https://sheets.googleapis.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-update-spreadsheet-values.md) for the provider-specific parameters and requirements.

