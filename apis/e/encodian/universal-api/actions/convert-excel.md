# Encodian: Convert Excel

Converts an Excel file in Encodian.

```
POST https://connect.mindcloud.co/v1/universal/encodian/latest/actions/convert-excel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/convert-excel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "outputFormat": "PDF",
  "filename": "hello.csv",
  "fileContent": "Base64 encoded Excel or CSV file content"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodian/latest/actions/convert-excel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "outputFormat": "PDF",
    "filename": "hello.csv",
    "fileContent": "Base64 encoded Excel or CSV file content"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `outputFormat` | string | yes | Default: `PDF`. Example: `PDF`. |
| `filename` | string | yes | Example: `hello.csv`. |
| `fileContent` | string | yes | Example: `Base64 encoded Excel or CSV file content`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `autoFit` | boolean | no |  |
| `worksheet` | string | no | Example: `Sheet1`. |
| `onePagePerSheet` | boolean | no |  |
| `allColumnsInOnePagePerSheetName` | boolean | no |  |
| `removeMarkup` | boolean | no |  |
| `exportHiddenSheets` | boolean | no |  |
| `csvDelimiter` | string | no | Example: `,`. |
| `cultureName` | string | no | Example: `en-US`. |
| `generateBookmarks` | boolean | no |  |
| `pdfACompliant` | boolean | no |  |
| `pdfAComplianceLevel` | string | no | Example: `1b`. |
| `compression` | string | no | Example: `LZW`. |

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

Through the native Encodian API, this operation is `POST /api/v1/Conversion/ConvertExcel` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-excel.md) for the provider-specific parameters and requirements.

