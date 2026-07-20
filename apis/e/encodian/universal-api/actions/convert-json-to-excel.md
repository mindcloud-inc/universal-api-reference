# Encodian: Convert JSON To Excel

Converts JSON data to Excel in Encodian.

```
POST https://connect.mindcloud.co/v1/universal/encodian/latest/actions/convert-json-to-excel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/convert-json-to-excel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "outputFilename": "output.xlsx"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodian/latest/actions/convert-json-to-excel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "outputFilename": "output.xlsx"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `outputFilename` | string | yes | The filename including extension of the output document. Example: `output.xlsx`. |
| `fileContent` | string | no | Optional base64 encoded representation of the JSON file to process. Example: `base64-encoded-json-file`. |
| `jsonData` | string | no | Optional JSON data string to process. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstRow` | number | no | The first row to be written to. |
| `firstColumn` | number | no | The first column to be written to. |
| `worksheetName` | string | no | The worksheet name that the JSON data is added to. Example: `Sheet1`. |
| `convertNumericAndDate` | boolean | no | Auto parse numeric and date values and set matching cell formats. |
| `dateFormat` | string | no | Custom date and time format string. Example: `yyyy-MM-dd`. |
| `numericFormat` | string | no | Numeric format string. Example: `0.00`. |
| `ignoreNullValues` | boolean | no | Ignore JSON properties that contain null values. |
| `titleFontColor` | string | no | The title font color. Example: `#1F4E79`. |
| `titleFontBold` | boolean | no | Set the title text to bold. |
| `titleWrapText` | boolean | no | Set whether title text wraps. |
| `ignoreAttributeTitles` | boolean | no | Ignore JSON attribute titles in the output workbook. |
| `cultureName` | string | no | Set the workbook culture before conversion. Example: `en-GB`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ],
      "fileContent": "string",
      "filename": "Ava Chen",
      "httpStatusCode": 1,
      "httpStatusMessage": "string",
      "operationId": "string",
      "operationStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> |  |
| `fileContent` | string |  |
| `filename` | string |  |
| `httpStatusCode` | number |  |
| `httpStatusMessage` | string |  |
| `operationId` | string |  |
| `operationStatus` | string |  |

## Native endpoint

Through the native Encodian API, this operation is `POST /api/v1/Conversion/ConvertJsonToExcel` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-json-to-excel.md) for the provider-specific parameters and requirements.

