# Download Excel URL with DocuPipe

Retrieves an Excel download URL from DocuPipe.

## Endpoint

- **Method:** `GET`
- **Path:** `/standardization/:standardizationId/download/excel-url`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Download Excel URL](https://docs.docupipe.ai/reference/download_excel_url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `standardization_id` | path | `string` | yes | — |
| `hours` | query | `number` | no | Number of hours the URL should be valid for |
