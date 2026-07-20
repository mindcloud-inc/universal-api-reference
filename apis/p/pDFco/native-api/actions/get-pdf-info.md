# Get PDF Info with PDF.co

Retrieves PDF info from PDF.co.

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf/info`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [Get PDF Info](https://docs.pdf.co/api-tester/pdf-info-reader)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | URL of the PDF file to inspect. |
| `password` | body | `string` | no | Password for protected PDFs. |
| `async` | body | `boolean` | no | Process info extraction as background job. |
