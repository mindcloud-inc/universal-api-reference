# Excel to PDF with PDF.co

Creates a PDF from Excel in PDF.co.

## Endpoint

- **Method:** `POST`
- **Path:** `/xls/convert/to/pdf`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [Excel to PDF](https://docs.pdf.co/api-reference/convert-from-excel/pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the Excel file to convert. |
| `name` | body | `string` | no | Optional output PDF file name. |
