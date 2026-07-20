# Google Sheets: Get Spreadsheet Metadata

Retrieves spreadsheet metadata from Google Sheets.

```
GET https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/get-spreadsheet-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Sheets `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `spreadsheetId` | list<list> | yes | Select a spreadsheet from the list. If you do not see the spreadsheet, click {} and paste the spreadsheet ID from a List Spreadsheets step or directly from the Google Sheets URL. Example: `Select a spreadsheet, or click {} to paste a spreadsheet ID`. |
| `ranges` | string | no |  |
| `includeGridData` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Sheets API returns.

## Native endpoint

Through the native Google Sheets API, this operation is `GET spreadsheets/:spreadsheetId` (base URL `https://sheets.googleapis.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-spreadsheet-metadata.md) for the provider-specific parameters and requirements.

