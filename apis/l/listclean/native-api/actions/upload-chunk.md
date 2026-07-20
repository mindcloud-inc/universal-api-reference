# Upload Chunk with Listclean

Uploads a CSV chunk to Listclean.

## Endpoint

- **Method:** `POST`
- **Path:** `/uploads/:upload_id`
- **Base URL:** `https://api.listclean.xyz/v1`
- **Official documentation:** [Upload Chunk](https://api.listclean.xyz/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `upload_id` | path | `number` | yes | Upload ID returned by Start Upload. |
| `chunk_sequence_number` | body | `number` | yes | Sequence number for this chunk. |
| `content` | body | `string` | yes | Base64-encoded contents of the file chunk. |
| `md5_checksum` | body | `string` | no | Optional MD5 hash for file integrity checking. |
