# Swiss QR Code - Read from Image with Encodian - Barcode

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Barcodes/ReadSwissQrCodeFromImage`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Swiss QR Code - Read from Image](https://support.encodian.com/hc/en-gb/articles/22624743460892)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | Base64 source image file content. |
| `barcodeRemoveControlChars` | body | `boolean` | no | Remove recognized control characters from decoded values. |
