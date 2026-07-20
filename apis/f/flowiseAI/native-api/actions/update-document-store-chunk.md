# Update Document Store Chunk with FlowiseAI

Updates a specific document chunk in FlowiseAI.

## Endpoint

- **Method:** `PUT`
- **Path:** `/document-store/chunks/{storeId}/{loaderId}/{chunkId}`
- **Base URL:** `https://cloud.flowiseai.com/api/v1`
- **Official documentation:** [Update Document Store Chunk](https://docs.flowiseai.com/api-reference/document-store)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | no | JSON body with documented chunk fields to update. |
| `chunkId` | path | `string` | yes | Document store chunk ID. |
| `loaderId` | path | `string` | yes | Document loader ID containing the chunk. |
| `storeId` | path | `string` | yes | Document store ID containing the chunk. |
