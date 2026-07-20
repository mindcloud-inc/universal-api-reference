# Encodian - Barcode: QR Code - Read from Image



```
GET https://connect.mindcloud.co/v1/universal/encodianBarcode/latest/actions/qr-code-read-from-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Barcode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianBarcode/latest/actions/qr-code-read-from-image?connectionId=$CONNECTION_ID&fileContent=string&barcodeImageFormat=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileContent": "string",
  "barcodeImageFormat": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianBarcode/latest/actions/qr-code-read-from-image?${params}`, {
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
| `fileContent` | string | yes | Base64 source image file content. |
| `barcodeImageFormat` | string | yes | Image format of the source QR code image. One of: `0`, `1`, `2`, `3`, `4`, `5`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `barcodeReadConfidence` | string | no | Confidence level for QR code detection. |
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
      "Value": "string"
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
| `Value` | string | QR code value detected in the image. |

## Native endpoint

Through the native Encodian - Barcode API, this operation is `POST /api/v1/Barcodes/ReadQrCodeFromImage` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/qr-code-read-from-image.md) for the provider-specific parameters and requirements.

