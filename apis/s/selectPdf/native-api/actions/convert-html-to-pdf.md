# Convert HTML to PDF with SelectPdf

## Endpoint

- **Method:** `POST`
- **Path:** `/convert/`
- **Base URL:** `https://selectpdf.com/api2`
- **Official documentation:** [Convert HTML to PDF](https://selectpdf.com/html-to-pdf-api/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html` | body | `string` | yes | Raw HTML markup to convert into a PDF. |
| `base_url` | body | `string` | no | Optional base URL used to resolve relative paths inside the HTML markup. |
