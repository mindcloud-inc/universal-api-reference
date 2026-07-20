# Download Excel URL with DocuPanda - Document Understanding

Retrieves a standardization Excel download URL from DocuPanda.

## Endpoint

- **Method:** `GET`
- **Path:** `/standardization/:standardization_id/download/excel-url`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Download Excel URL](https://docs.docupipe.ai/reference/download_excel_url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hours` | query | `number` | no | Number of hours the URL should be valid for |
| `standardization_id` | path | `string` | yes | — |
