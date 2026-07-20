# Download Original URL with DocuPipe

Retrieves an original document download URL from DocuPipe.

## Endpoint

- **Method:** `GET`
- **Path:** `/document/:documentId/download/original-url`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Download Original URL](https://docs.docupipe.ai/reference/download_original_url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | — |
| `hours` | query | `number` | no | Number of hours the URL should be valid for |
| `format` | query | `list` | no | Output format of the document Accepted values: `original`, `pdf`, `uploaded`. |
