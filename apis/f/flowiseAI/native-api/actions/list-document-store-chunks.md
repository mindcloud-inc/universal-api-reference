# List Document Store Chunks with FlowiseAI

Retrieves chunks from a FlowiseAI document loader.

## Endpoint

- **Method:** `GET`
- **Path:** `/document-store/chunks/{storeId}/{loaderId}/{pageNo}`
- **Base URL:** `https://cloud.flowiseai.com/api/v1`
- **Official documentation:** [List Document Store Chunks](https://docs.flowiseai.com/api-reference/document-store)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `loaderId` | path | `string` | yes | Document loader ID within the document store. |
| `pageNo` | path | `number` | yes | Pagination number for document store chunks. |
| `storeId` | path | `string` | yes | Document store ID for chunk listing. |
