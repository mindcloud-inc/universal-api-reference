# PDF-app: Create QR Code Or Barcode

Creates a QR code or barcode in PDF-app.

```
POST https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/create-qr-code-or-barcode
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF-app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/create-qr-code-or-barcode" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "texts[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/create-qr-code-or-barcode', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "texts[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Choose whether to generate a qr code or a barcode. |
| `texts[]` | array<string> | yes | Array of text values to encode into the generated qr codes or barcodes. |
| `fileName` | string | no | Optional base filename for the generated output files. |
| `size` | number | no | QR code size in pixels. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `margin` | number | no | QR code margin. |
| `color` | string | no | Foreground color for the generated code. |
| `backgroundColor` | string | no | Background color for qr generation. |
| `format` | string | no | Output image format, such as jpeg or png. |
| `width` | number | no | Barcode bar width. |
| `height` | number | no | Barcode height. |
| `includeText` | boolean | no | Whether to include readable text below the barcode. |
| `textXAlign` | string | no | Horizontal alignment for barcode text. |
| `textPadding` | number | no | Padding between the barcode and its text. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PDF-app API returns.

## Native endpoint

Through the native PDF-app API, this operation is `POST /qrCode` (base URL `https://api.pdf-app.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-qr-code-or-barcode.md) for the provider-specific parameters and requirements.

