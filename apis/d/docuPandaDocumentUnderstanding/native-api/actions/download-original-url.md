# Download Original URL with DocuPanda - Document Understanding

Retrieves an original document download URL from DocuPanda.

## Endpoint

- **Method:** `GET`
- **Path:** `/document/:document_id/download/original-url`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Download Original URL](https://docs.docupipe.ai/reference/download_original_url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | — |
| `format` | query | `string` | no | Output format of the document |
| `hours` | query | `number` | no | Number of hours the URL should be valid for |
