# Extract Receipt Data From Text with WiseOCR

Retrieves extracted receipt data from WiseOCR using text.

## Endpoint

- **Method:** `POST`
- **Path:** `/text`
- **Base URL:** `https://api.wiseocr.com/v1`
- **Official documentation:** [Extract Receipt Data From Text](https://developers.wiseocr.com/text-data-extraction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Text content of the receipt or invoice. |
| `skipItems` | body | `boolean` | no | Skip detailed line item extraction to speed up processing. |
