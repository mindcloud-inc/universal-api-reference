# Encodian - Barcode: QR Code - Read Document Status



```
GET https://connect.mindcloud.co/v1/universal/encodianBarcode/latest/actions/qr-code-read-document-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Barcode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianBarcode/latest/actions/qr-code-read-document-status?connectionId=$CONNECTION_ID&operationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "operationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianBarcode/latest/actions/qr-code-read-document-status?${params}`, {
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
| `operationId` | string | yes | Operation ID returned by QR Code - Read from Document. |

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
      "qrCodes": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Errors` | array<string> | Error messages returned by Encodian. |
| `HttpStatusCode` | number | HTTP status code. |
| `HttpStatusMessage` | string | HTTP status message. |
| `OperationId` | string | Operation ID. |
| `OperationStatus` | string | Encodian operation status. |
| `qrCodes` | array<string> | QR code values detected in the document. |

## Native endpoint

Through the native Encodian - Barcode API, this operation is `GET /api/v1/Barcodes/GetOperationStatusReadQrCodeFromDocument` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/qr-code-read-document-status.md) for the provider-specific parameters and requirements.

