# Google Sheets: Create Spreadsheet

Creates a new spreadsheet in Google Sheets.

```
POST https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/create-spreadsheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Sheets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/create-spreadsheet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/create-spreadsheet', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | no |  |

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
        "spreadsheetTheme": {
          "primaryFontFamily": "string",
          "themeColors": [
            {
              "colorType": "string"
            }
          ]
        },
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
| `properties.autoRecalc` | string |  |
| `properties.defaultFormat.backgroundColor.blue` | number |  |
| `properties.defaultFormat.backgroundColor.green` | number |  |
| `properties.defaultFormat.backgroundColor.red` | number |  |
| `properties.defaultFormat.backgroundColorStyle.rgbColor.blue` | number |  |
| `properties.defaultFormat.backgroundColorStyle.rgbColor.green` | number |  |
| `properties.defaultFormat.backgroundColorStyle.rgbColor.red` | number |  |
| `properties.defaultFormat.padding.bottom` | number |  |
| `properties.defaultFormat.padding.left` | number |  |
| `properties.defaultFormat.padding.right` | number |  |
| `properties.defaultFormat.padding.top` | number |  |
| `properties.defaultFormat.textFormat.bold` | boolean |  |
| `properties.defaultFormat.textFormat.fontFamily` | string |  |
| `properties.defaultFormat.textFormat.fontSize` | number |  |
| `properties.defaultFormat.textFormat.italic` | boolean |  |
| `properties.defaultFormat.textFormat.strikethrough` | boolean |  |
| `properties.defaultFormat.textFormat.underline` | boolean |  |
| `properties.defaultFormat.verticalAlignment` | string |  |
| `properties.defaultFormat.wrapStrategy` | string |  |
| `properties.locale` | string |  |
| `properties.spreadsheetTheme.primaryFontFamily` | string |  |
| `properties.spreadsheetTheme.themeColors[].colorType` | string |  |
| `properties.timeZone` | string |  |
| `properties.title` | string |  |
| `sheets[].properties.gridProperties.columnCount` | number |  |
| `sheets[].properties.gridProperties.rowCount` | number |  |
| `sheets[].properties.index` | number |  |
| `sheets[].properties.sheetId` | number |  |
| `sheets[].properties.sheetType` | string |  |
| `sheets[].properties.title` | string |  |
| `spreadsheetId` | string |  |
| `spreadsheetUrl` | string |  |

## Native endpoint

Through the native Google Sheets API, this operation is `POST spreadsheets` (base URL `https://sheets.googleapis.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-spreadsheet.md) for the provider-specific parameters and requirements.

