# Read Barcode from Image with PDF4me Image

Retrieves barcode data from an image in PDF4me Image.

## Endpoint

- **Method:** `POST`
- **Path:** `/ReadBarcodesfromImage`
- **Base URL:** `https://api.pdf4me.com/api/v2`
- **Official documentation:** [Read Barcode from Image](https://docs.pdf4me.com/url-api-tester/read-barcode-from-image/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docContent` | body | `string` | yes | Base64-encoded source image content. |
| `docName` | body | `string` | yes | Filename for the source image. |
