# Convert PDF To Excel with Encodian

Converts a PDF document to Excel in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/ConvertPdfToExcel`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert PDF To Excel](https://support.encodian.com/hc/en-gb/articles/17011591184284)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FileContent` | body | `string` | yes | A Base64 encoded representation of the PDF file to be processed. |
