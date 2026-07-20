# QR Code - Read from Image with Encodian - Barcode

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Barcodes/ReadQrCodeFromImage`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [QR Code - Read from Image](https://support.encodian.com/hc/en-gb/articles/360006170898-Read-QR-Code-Image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | Base64 source image file content. |
| `barcodeImageFormat` | body | `string` | yes | Image format of the source QR code image. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. |
| `barcodeReadConfidence` | body | `string` | no | Confidence level for QR code detection. |
| `barcodeRemoveControlChars` | body | `boolean` | no | Remove recognized control characters from decoded values. |
