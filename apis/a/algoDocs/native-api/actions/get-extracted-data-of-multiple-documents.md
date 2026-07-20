# Get Extracted Data of Multiple Documents with AlgoDocs

Retrieves extracted data from AlgoDocs documents by extractor.

## Endpoint

- **Method:** `GET`
- **Path:** `/extracted_data/:extractorId`
- **Base URL:** `https://api.algodocs.com/v1`
- **Official documentation:** [Get Extracted Data of Multiple Documents](https://api.algodocs.com/#extracted_data_multiple_documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `extractorId` | path | `string` | yes | The extractor ID from your AlgoDocs account. |
| `folderId` | query | `string` | no | Optional folder filter for extracted data results. |
| `date` | query | `string` | no | Optional ISO 8601 date filter for documents uploaded after this date. |
