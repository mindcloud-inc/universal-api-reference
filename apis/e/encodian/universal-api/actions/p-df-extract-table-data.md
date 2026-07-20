# Encodian: PDF Extract Table Data

Extracts PDF table data in Encodian.

```
GET https://connect.mindcloud.co/v1/universal/encodian/latest/actions/p-df-extract-table-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/p-df-extract-table-data?connectionId=$CONNECTION_ID&fileContent=string&extract=First" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileContent": "string",
  "extract": "First"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodian/latest/actions/p-df-extract-table-data?${params}`, {
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
| `fileContent` | string | yes | A Base64 encoded representation of the PDF file to be processed. |
| `extract` | string | yes | Specify the table to extract. Example: `First`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startPage` | number | no | Specifies the page number to start extracting tables from. |
| `endPage` | number | no | Specifies the page number to stop extracting tables on. |
| `tableIndex` | number | no | If Extract is set to Custom, specify the index of the table to extract. |
| `hasHeaderRow` | boolean | no | Set whether the first row is a header row. |

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
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> | Errors returned by Encodian, if any. |
| `httpStatusCode` | number | The HTTP status code returned by Encodian. |
| `httpStatusMessage` | string | The HTTP status message returned by Encodian. |
| `operationId` | string | The Encodian operation ID. |
| `operationStatus` | string | The Encodian operation status. |
| `result` | string | The extracted table data as a JSON string. |

## Native endpoint

Through the native Encodian API, this operation is `POST /api/v1/PDF/PdfExtractTableData` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/p-df-extract-table-data.md) for the provider-specific parameters and requirements.

