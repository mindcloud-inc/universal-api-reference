# Start OCR PDF Task with iLovePDFv2

Starts a PDF OCR task in iLovePDFv2.

## Endpoint

- **Method:** `GET`
- **Path:** `/start/pdfocr/:region`
- **Base URL:** `https://api.ilovepdf.com/v1`
- **Official documentation:** [Start OCR PDF Task](https://www.iloveapi.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `region` | path | `list` | yes | Processing region / jurisdiction. Accepted values: `0`, `1`, `2`, `3`, `4`. |
