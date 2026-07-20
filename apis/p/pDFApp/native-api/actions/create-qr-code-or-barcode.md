# Create QR Code Or Barcode with PDF-app

Creates a QR code or barcode in PDF-app.

## Endpoint

- **Method:** `POST`
- **Path:** `/qrCode`
- **Base URL:** `https://api.pdf-app.net`
- **Official documentation:** [Create QR Code Or Barcode](https://pdf-app.net/apidocumentation?type=qrCode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Choose whether to generate a qr code or a barcode. |
| `texts[]` | body | `array<string>` | yes | Array of text values to encode into the generated qr codes or barcodes. |
| `filename` | body | `string` | no | Optional base filename for the generated output files. |
| `size` | body | `number` | no | QR code size in pixels. |
| `margin` | body | `number` | no | QR code margin. |
| `color` | body | `string` | no | Foreground color for the generated code. |
| `backgroundColor` | body | `string` | no | Background color for qr generation. |
| `format` | body | `string` | no | Output image format, such as jpeg or png. |
| `width` | body | `number` | no | Barcode bar width. |
| `height` | body | `number` | no | Barcode height. |
| `includetext` | body | `boolean` | no | Whether to include readable text below the barcode. |
| `textxalign` | body | `string` | no | Horizontal alignment for barcode text. |
| `textpadding` | body | `number` | no | Padding between the barcode and its text. |
