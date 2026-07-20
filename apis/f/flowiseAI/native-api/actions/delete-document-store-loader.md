# Delete Document Store Loader with FlowiseAI

Deletes a document loader and chunks from FlowiseAI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/document-store/loader/{storeId}/{loaderId}`
- **Base URL:** `https://cloud.flowiseai.com/api/v1`
- **Official documentation:** [Delete Document Store Loader](https://docs.flowiseai.com/api-reference/document-store)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `loaderId` | path | `string` | yes | Loader ID within the document store. |
| `storeId` | path | `string` | yes | Document store ID. |
