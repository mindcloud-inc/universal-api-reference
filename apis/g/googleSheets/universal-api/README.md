# <img src="https://images.mindcloud.co/apps/icons/google-sheets-logo-512px_1781814064500.png" alt="Google Sheets logo" width="28" height="28"> Google Sheets: Universal API

Build spreadsheets, analyze data, collaborate in real time, and visualize insights.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/googleSheets/latest
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.google.com/sheets

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Spreadsheet Metadata](actions/get-spreadsheet-metadata.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/get-spreadsheet-metadata?connectionId=$CONNECTION_ID&spreadsheetId=Select%20a%20spreadsheet%2C%20or%20click%20%7B%7D%20to%20paste%20a%20spreadsheet%20ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Cell

| Action | Method | Description |
| --- | --- | --- |
| [Update Cell](actions/update-cell.md) | PUT | Updates a cell in a Google Sheets worksheet. |

### Column

| Action | Method | Description |
| --- | --- | --- |
| [List Spreadsheet Columns](actions/list-spreadsheet-columns.md) | GET | Retrieves columns from a Google Sheets worksheet. |

### Row

| Action | Method | Description |
| --- | --- | --- |
| [Append Rows](actions/append-rows.md) | POST | Appends rows to a Google Sheets worksheet. |
| [Clear Row](actions/clear-row.md) | DELETE | Clears row contents in Google Sheets while keeping rows intact. |
| [Create Row](actions/create-row.md) | POST | Creates a new row in a Google Sheets worksheet. |
| [Delete Row](actions/delete-row.md) | DELETE | Deletes a row from a Google Sheets worksheet. |
| [Delete Rows](actions/delete-rows.md) | DELETE | Deletes multiple rows from a Google Sheets worksheet. |
| [List Spreadsheet Rows](actions/list-spreadsheet-rows.md) | GET | Retrieves rows from a Google Sheets worksheet. |
| [Update Spreadsheet Row](actions/update-spreadsheet-row.md) | PUT | Updates a row in a Google Sheets worksheet. |

### Spreadsheet

| Action | Method | Description |
| --- | --- | --- |
| [Batch Update Spreadsheet Values](actions/batch-update-spreadsheet-values.md) | PUT | Updates explicit A1 ranges in Google Sheets. |
| [Create Spreadsheet](actions/create-spreadsheet.md) | POST | Creates a new spreadsheet in Google Sheets. |
| [Create Worksheet](actions/create-worksheet.md) | POST | Creates a new worksheet in Google Sheets. |
| [Get Spreadsheet Metadata](actions/get-spreadsheet-metadata.md) | GET | Retrieves spreadsheet metadata from Google Sheets. |
| [List Spreadsheets](actions/list-spreadsheets.md) | GET | Retrieves accessible Google Sheets files from Google Drive. |

### Worksheets

| Action | Method | Description |
| --- | --- | --- |
| [List Spreadsheet Worksheets](actions/list-spreadsheet-worksheets.md) | GET | Retrieves worksheets from a Google Sheets spreadsheet. |

