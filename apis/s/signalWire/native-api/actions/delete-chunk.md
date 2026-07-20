# Delete Chunk with SignalWire

Deletes an existing chunk from SignalWire.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/datasphere/documents/{documentId}/chunks/{chunkId}`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Delete Chunk](https://signalwire.com/docs/apis/rest/chunks/delete-document-chunk)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | Unique ID of the parent Document. |
| `chunkId` | path | `string` | yes | Unique ID of a Chunk. |
