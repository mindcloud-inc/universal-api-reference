# Encodian: Excel Extract Rows

Extracts Excel rows in Encodian.

```
GET https://connect.mindcloud.co/v1/universal/encodian/latest/actions/excel-extract-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/excel-extract-rows?connectionId=$CONNECTION_ID&fileContent=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileContent": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodian/latest/actions/excel-extract-rows?${params}`, {
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
| `fileContent` | string | yes | A Base64 encoded representation of the Excel file to be processed. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `worksheetName` | string | no | Set the name of a specific worksheet to be exported. |
| `hasHeaderRow` | boolean | no | Set whether the worksheet has a header row. |
| `firstRow` | number | no | Set the number of the first row to be exported. |
| `lastRow` | number | no | Set the number of the last row to be exported. |
| `firstColumn` | number | no | Set the number of the first column to be exported. |
| `lastColumn` | number | no | Set the number of the last column to be exported. |
| `excludeEmptyRows` | boolean | no | Set whether empty rows should be excluded from the export. |
| `exportEmptyCells` | boolean | no | Set whether empty cells should be exported. |
| `exportValuesAsText` | boolean | no | Set whether values should be exported as text. |
| `hyperlinkFormat` | string | no | Set how hyperlinks should be exported. |
| `exportAsObject` | boolean | no | Force row data to be exported as an object. |
| `excludeHiddenRows` | boolean | no | Set whether hidden rows should be excluded from the export. |
| `excludeHiddenColumns` | boolean | no | Set whether hidden columns should be excluded from the export. |
| `culture` | string | no | Set the culture for the workbook prior to conversion. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ],
      "httpStatusCode": 1,
      "httpStatusMessage": "string",
      "operationId": "string",
      "operationStatus": "string",
      "rowData": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> |  |
| `httpStatusCode` | number |  |
| `httpStatusMessage` | string |  |
| `operationId` | string |  |
| `operationStatus` | string |  |
| `rowData` | string |  |

## Native endpoint

Through the native Encodian API, this operation is `POST /api/v1/Excel/GetRowsFromExcel` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/excel-extract-rows.md) for the provider-specific parameters and requirements.

