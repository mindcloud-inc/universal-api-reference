# Generate Barcodes with PDF.co

Creates barcodes in PDF.co.

## Endpoint

- **Method:** `POST`
- **Path:** `/barcode/generate`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [Generate Barcodes](https://docs.pdf.co/api-reference/barcode/generate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Barcode symbology type. |
| `value` | body | `string` | yes | Value to encode into barcode. |
| `name` | body | `string` | no | Optional output image file name. |
