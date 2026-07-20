# List Documents with DocuPanda - Document Understanding

Retrieves documents from DocuPanda.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [List Documents](https://docs.docupipe.ai/reference/list_documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | query | `string` | no | The dataset to filter documents by |
| `limit` | query | `number` | no | The maximum number of documents to return. Maximum is 1000 |
| `offset` | query | `number` | no | The number of documents to skip (to paginate through the dataset) |
| `exclude_payload` | query | `boolean` | no | Whether to exclude the result payload from the response |
