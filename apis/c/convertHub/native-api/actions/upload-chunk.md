# Upload Chunk with ConvertHub

Uploads one file chunk to ConvertHub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/upload/:sessionId/chunks/:chunkIndex`
- **Base URL:** `https://api.converthub.com/v2`
- **Official documentation:** [Upload Chunk](https://converthub.com/api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | — |
| `chunkIndex` | path | `number` | yes | — |
| `chunk` | body | `file` | yes | The chunk data |
