# Update Dataset with DocuPipe

Updates a dataset for DocuPipe documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/update-dataset`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Update Dataset](https://docs.docupipe.ai/reference/update_documents_dataset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentIds[]` | body | `array<string>` | yes | List of document IDs to update. |
| `dataset` | body | `string` | yes | Name of the dataset to which you want to assign these documents. |
