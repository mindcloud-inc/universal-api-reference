# QR Code - Create with Encodian - Barcode

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Barcodes/CreateQrCode`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [QR Code - Create](https://support.encodian.com/hc/en-gb/articles/360005178237-Create-QR-Code)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `barcodeData` | body | `string` | yes | Text value encoded into the QR code. |
| `barcodeImageFormat` | body | `string` | yes | Output image format for the generated QR code. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. |
| `width` | body | `number` | no | QR code width in pixels. |
| `height` | body | `number` | no | QR code height in pixels. |
| `foreColor` | body | `string` | no | QR code foreground color as an HTML color value. |
| `backColor` | body | `string` | no | QR code background color as an HTML color value. |
| `logoFileContent` | body | `file` | no | Optional source logo file content to embed in the QR code. |
