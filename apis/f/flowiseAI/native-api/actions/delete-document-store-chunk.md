# Delete Document Store Chunk with FlowiseAI

Deletes a specific document chunk from FlowiseAI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/document-store/chunks/{storeId}/{loaderId}/{chunkId}`
- **Base URL:** `https://cloud.flowiseai.com/api/v1`
- **Official documentation:** [Delete Document Store Chunk](https://docs.flowiseai.com/api-reference/document-store)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chunkId` | path | `string` | yes | Document store chunk ID to delete. |
| `loaderId` | path | `string` | yes | Document loader ID containing the chunk. |
| `storeId` | path | `string` | yes | Document store ID containing the chunk. |
