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

```json
{
  "success": true,
  "data": [
    {
      "properties": {
        "autoRecalc": "string",
        "defaultFormat": {
          "backgroundColor": {
            "blue": 1,
            "green": 1,
            "red": 1
          },
          "backgroundColorStyle": {
            "rgbColor": {
              "blue": 1,
              "green": 1,
              "red": 1
            }
          },
          "padding": {
            "bottom": 1,
            "left": 1,
            "right": 1,
            "top": 1
          },
          "textFormat": {
            "bold": true,
            "fontFamily": "string",
            "fontSize": 1,
            "italic": true,
            "strikethrough": true,
            "underline": true
          },
          "verticalAlignment": "string",
          "wrapStrategy": "string"
        },
        "locale": "string",
        "timeZone": "string",
        "title": "string"
      },
      "sheets": [
        {
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
      ],
      "spreadsheetId": "string",
      "spreadsheetUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `properties.autoRecalc` | string | The recalculation setting of the spreadsheet. |
| `properties.defaultFormat.backgroundColor.blue` | number | The blue component of the default background color. |
| `properties.defaultFormat.backgroundColor.green` | number | The green component of the default background color. |
| `properties.defaultFormat.backgroundColor.red` | number | The red component of the default background color. |
| `properties.defaultFormat.backgroundColorStyle.rgbColor.blue` | number | The blue component of the default background color style. |
| `properties.defaultFormat.backgroundColorStyle.rgbColor.green` | number | The green component of the default background color style. |
| `properties.defaultFormat.backgroundColorStyle.rgbColor.red` | number | The red component of the default background color style. |
| `properties.defaultFormat.padding.bottom` | number | The bottom padding of the default cell format, in pixels. |
| `properties.defaultFormat.padding.left` | number | The left padding of the default cell format, in pixels. |
| `properties.defaultFormat.padding.right` | number | The right padding of the default cell format, in pixels. |
| `properties.defaultFormat.padding.top` | number | The top padding of the default cell format, in pixels. |
| `properties.defaultFormat.textFormat.bold` | boolean | Whether the default text is bold. |
| `properties.defaultFormat.textFormat.fontFamily` | string | The default font family of the spreadsheet. |
| `properties.defaultFormat.textFormat.fontSize` | number | The default font size of the spreadsheet. |
| `properties.defaultFormat.textFormat.italic` | boolean | Whether the default text is italic. |
| `properties.defaultFormat.textFormat.strikethrough` | boolean | Whether the default text is struck through. |
| `properties.defaultFormat.textFormat.underline` | boolean | Whether the default text is underlined. |
| `properties.defaultFormat.verticalAlignment` | string | The default vertical alignment of cells. |
| `properties.defaultFormat.wrapStrategy` | string | The default text wrap strategy of cells. |
| `properties.locale` | string | The locale of the spreadsheet. |
| `properties.timeZone` | string | The time zone of the spreadsheet. |
| `properties.title` | string | The title of the spreadsheet. |
| `sheets[].properties.gridProperties.columnCount` | number | The number of columns in the worksheet grid. |
| `sheets[].properties.gridProperties.rowCount` | number | The number of rows in the worksheet grid. |
| `sheets[].properties.index` | number | The index of the worksheet. |
| `sheets[].properties.sheetId` | number | The ID of the worksheet. |
| `sheets[].properties.sheetType` | string | The type of the worksheet. |
| `sheets[].properties.title` | string | The title of the worksheet. |
| `spreadsheetId` | string | The unique identifier of the spreadsheet. |
| `spreadsheetUrl` | string | The URL of the spreadsheet. |

## Native endpoint

Through the native Google Sheets API, this operation is `GET spreadsheets/:spreadsheetId` (base URL `https://sheets.googleapis.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-spreadsheet-metadata.md) for the provider-specific parameters and requirements.

