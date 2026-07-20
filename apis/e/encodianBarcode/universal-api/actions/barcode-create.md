# Encodian - Barcode: Barcode - Create



```
POST https://connect.mindcloud.co/v1/universal/encodianBarcode/latest/actions/barcode-create
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Barcode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodianBarcode/latest/actions/barcode-create" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "barcodeType": "0",
  "barcodeData": "string",
  "barcodeImageFormat": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodianBarcode/latest/actions/barcode-create', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "barcodeType": "0",
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
| `barcodeType` | string | yes | Barcode symbology to generate, such as Code128, QR-compatible two-dimensional types, EAN13, or UPCA. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |
| `barcodeData` | string | yes | Text value encoded into the barcode. |
| `barcodeImageFormat` | string | yes | Output image format for the generated barcode. One of: `0`, `1`, `2`, `3`, `4`, `5`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `width` | number | no | Barcode image width in pixels. |
| `height` | number | no | Barcode image height in pixels. |
| `barColor` | string | no | Barcode bar color as an HTML color value. Example: `#000000`. |
| `sizeMode` | string | no | Barcode auto sizing mode. One of: `0`, `1`, `2`, `3`. |

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
| `FileContent` | string | Generated barcode image file content. |
| `Filename` | string | Generated barcode image filename. |
| `HttpStatusCode` | number | HTTP status code returned by Encodian. |
| `HttpStatusMessage` | string | HTTP status message returned by Encodian. |
| `OperationId` | string | Encodian operation identifier. |
| `OperationStatus` | string | Encodian operation status. |

## Native endpoint

Through the native Encodian - Barcode API, this operation is `POST /api/v1/Barcodes/CreateBarcode` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/barcode-create.md) for the provider-specific parameters and requirements.

