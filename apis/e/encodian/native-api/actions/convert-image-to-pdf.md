# Convert Image To PDF with Encodian

Converts an image to PDF in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/ConvertImageToPdf`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert Image To PDF](https://support.encodian.com/hc/en-gb/articles/23601928355228)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ocrType` | body | `string` | yes |
| `fileContent` | body | `string` | yes |
| `ocrLanguage` | body | `string` | no |
| `returnFile` | body | `boolean` | no |
