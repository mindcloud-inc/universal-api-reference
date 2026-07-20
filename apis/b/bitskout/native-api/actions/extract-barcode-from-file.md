# Extract Barcode from File with Bitskout

Extracts barcode values from a file with Bitskout.

## Endpoint

- **Method:** `POST`
- **Path:** `/actions/barcodes`
- **Base URL:** `https://api.bitskout.com/v2`
- **Official documentation:** [Extract Barcode from File](https://learn.microsoft.com/en-us/connectors/bitskout/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_url` | body | `string` | no | Direct download URL for the file that contains a barcode. |
