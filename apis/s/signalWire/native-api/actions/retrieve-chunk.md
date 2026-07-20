# Retrieve Chunk with SignalWire

Retrieves a chunk from SignalWire.

## Endpoint

- **Method:** `GET`
- **Path:** `/datasphere/documents/{documentId}/chunks/{chunkId}`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Retrieve Chunk](https://signalwire.com/docs/apis/rest/chunks/get-document-chunk)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | Unique ID of the parent Document. |
| `chunkId` | path | `string` | yes | Unique ID of a Chunk. |
