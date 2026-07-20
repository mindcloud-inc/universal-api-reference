# Read Barcodes with PDF.co

Reads barcodes from a file in PDF.co.

## Endpoint

- **Method:** `POST`
- **Path:** `/barcode/read/from/url`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [Read Barcodes](https://docs.pdf.co/api-reference/barcode/read)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | URL of image or PDF containing barcodes. |
| `types` | body | `string` | no | Optional list of barcode types to detect. |
