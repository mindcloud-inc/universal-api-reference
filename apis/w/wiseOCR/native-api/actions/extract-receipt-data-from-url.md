# Extract Receipt Data From URL with WiseOCR

Retrieves extracted receipt data from WiseOCR using a file URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/url`
- **Base URL:** `https://api.wiseocr.com/v1`
- **Official documentation:** [Extract Receipt Data From URL](https://developers.wiseocr.com/url-data-extraction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | URL of the receipt image or PDF file |
| `skipItems` | body | `boolean` | no | Skip detailed line item extraction to speed up processing |
