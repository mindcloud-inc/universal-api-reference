# Encodian - Barcode: Swiss QR Code - Read from Document



```
GET https://connect.mindcloud.co/v1/universal/encodianBarcode/latest/actions/swiss-qr-code-read-from-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Barcode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianBarcode/latest/actions/swiss-qr-code-read-from-document?connectionId=$CONNECTION_ID&fileContent=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileContent": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianBarcode/latest/actions/swiss-qr-code-read-from-document?${params}`, {
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
| `fileContent` | string | yes | Base64 source document file content. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `barcodeReadConfidence` | string | no | Confidence level for Swiss QR detection. |
| `barcodeReadQuality` | string | no | Quality level for Swiss QR detection. |
| `pageNumbers` | string | no | Comma-separated page numbers to inspect, such as 1,3,4. |
| `barcodeRemoveControlChars` | boolean | no | Remove recognized control characters from decoded values. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Errors": [
        "string"
      ],
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "OperationId": "string",
      "OperationStatus": "string",
      "swissQrCodes": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Errors` | array<string> |  |
| `HttpStatusCode` | number |  |
| `HttpStatusMessage` | string |  |
| `OperationId` | string |  |
| `OperationStatus` | string | Encodian operation status. |
| `swissQrCodes` | array<object> | Swiss QR code records detected in the document. |

## Native endpoint

Through the native Encodian - Barcode API, this operation is `POST /api/v1/Barcodes/ReadSwissQrCodesFromDocument` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/swiss-qr-code-read-from-document.md) for the provider-specific parameters and requirements.

