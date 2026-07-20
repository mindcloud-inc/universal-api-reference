# Barcode - Create with Encodian - Barcode

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Barcodes/CreateBarcode`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Barcode - Create](https://support.encodian.com/hc/en-gb/articles/360006165457-Create-Barcode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `barcodeTypeParameter` | query | `string` | yes | Barcode symbology to generate, such as Code128, QR-compatible two-dimensional types, EAN13, or UPCA. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |
| `barcodeData` | body | `string` | yes | Text value encoded into the barcode. |
| `barcodeImageFormat` | body | `string` | yes | Output image format for the generated barcode. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. |
| `width` | body | `number` | no | Barcode image width in pixels. |
| `height` | body | `number` | no | Barcode image height in pixels. |
| `barColor` | body | `string` | no | Barcode bar color as an HTML color value. |
| `sizeMode` | body | `string` | no | Barcode auto sizing mode. Accepted values: `0`, `1`, `2`, `3`. |
