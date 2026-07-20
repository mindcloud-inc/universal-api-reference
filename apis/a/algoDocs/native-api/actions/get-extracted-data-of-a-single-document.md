# Get Extracted Data of a Single Document with AlgoDocs

Retrieves extracted data from one AlgoDocs document.

## Endpoint

- **Method:** `GET`
- **Path:** `/extracted_data/:documentId`
- **Base URL:** `https://api.algodocs.com/v1`
- **Official documentation:** [Get Extracted Data of a Single Document](https://api.algodocs.com/#extracted-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | The document ID returned by an AlgoDocs upload action. |
