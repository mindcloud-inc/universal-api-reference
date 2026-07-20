# Encodian - Barcode: QR Code - Create



```
POST https://connect.mindcloud.co/v1/universal/encodianBarcode/latest/actions/qr-code-create
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Barcode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodianBarcode/latest/actions/qr-code-create" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "barcodeData": "string",
  "barcodeImageFormat": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodianBarcode/latest/actions/qr-code-create', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "barcodeData": "string",
    "barcodeImageFormat": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `barcodeData` | string | yes | Text value encoded into the QR code. |
| `barcodeImageFormat` | string | yes | Output image format for the generated QR code. One of: `0`, `1`, `2`, `3`, `4`, `5`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `width` | number | no | QR code width in pixels. |
| `height` | number | no | QR code height in pixels. |
| `foreColor` | string | no | QR code foreground color as an HTML color value. Example: `#000000`. |
| `backColor` | string | no | QR code background color as an HTML color value. Example: `#FFFFFF`. |
| `logoFileContent` | file | no | Optional source logo file content to embed in the QR code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Errors": [
        "string"
      ],
      "FileContent": "string",
      "Filename": "Ava Chen",
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "OperationId": "string",
      "OperationStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Errors` | array<string> | Error messages returned by Encodian. |
| `FileContent` | string | Generated QR code image file content. |
| `Filename` | string | Generated QR code image filename. |
| `HttpStatusCode` | number | HTTP status code returned by Encodian. |
| `HttpStatusMessage` | string | HTTP status message returned by Encodian. |
| `OperationId` | string | Encodian operation identifier. |
| `OperationStatus` | string | Encodian operation status. |

## Native endpoint

Through the native Encodian - Barcode API, this operation is `POST /api/v1/Barcodes/CreateQrCode` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/qr-code-create.md) for the provider-specific parameters and requirements.

