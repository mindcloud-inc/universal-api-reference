# Encodian: PDF Split By Barcode

Splits a PDF by barcode in Encodian.

```
DELETE https://connect.mindcloud.co/v1/universal/encodian/latest/actions/pdf-split-by-barcode
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/pdf-split-by-barcode?connectionId=$CONNECTION_ID&filename=Ava%20Chen&fileContent=string&splitPdfByBarcodeType=string&splitPdfByBarcodeAction=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filename": "Ava Chen",
  "fileContent": "string",
  "splitPdfByBarcodeType": "string",
  "splitPdfByBarcodeAction": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodian/latest/actions/pdf-split-by-barcode?${params}`, {
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
| `filename` | string | yes | The filename of the source PDF document including the file extension. |
| `fileContent` | string | yes | A Base64 encoded representation of the source PDF document. |
| `splitPdfByBarcodeType` | string | yes | Select whether to split on the first instance, last instance, or all instances matching the barcode value. |
| `splitPdfByBarcodeAction` | string | yes | Select whether to split on, before, after, or remove the page containing the barcode. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `splitPdfByBarcodeValue` | string | no | Optionally specify a whole barcode value to match. |
| `barcodeReadConfidence` | string | no | Set the confidence level for barcode detection. |
| `appendBarcodeValue` | boolean | no | Set whether to add the barcode value to the output filename. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documents": [
        {}
      ],
      "errors": [
        "string"
      ],
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
| `documents` | array<object> | The split PDF documents when Encodian has completed the operation. |
| `errors` | array<string> | Errors returned by Encodian, if any. |
| `httpStatusCode` | number | The HTTP status code returned by Encodian. |
| `httpStatusMessage` | string | The HTTP status message returned by Encodian. |
| `operationId` | string | The Encodian operation ID for the queued split operation. |
| `operationStatus` | string | The Encodian operation status. |

## Native endpoint

Through the native Encodian API, this operation is `POST /api/v1/PDF/SplitPdfByBarcode` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pdf-split-by-barcode.md) for the provider-specific parameters and requirements.

