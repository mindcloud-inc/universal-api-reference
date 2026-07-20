# Excel to CSV with PDF.co

Creates a CSV file from Excel in PDF.co.

## Endpoint

- **Method:** `POST`
- **Path:** `/xls/convert/to/csv`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [Excel to CSV](https://docs.pdf.co/api-reference/convert-from-excel/csv)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the Excel file to convert. |
| `name` | body | `string` | no | Optional output CSV file name. |
