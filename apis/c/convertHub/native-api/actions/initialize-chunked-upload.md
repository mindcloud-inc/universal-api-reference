# Initialize Chunked Upload with ConvertHub

Creates a chunked upload session in ConvertHub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/upload/init`
- **Base URL:** `https://api.converthub.com/v2`
- **Official documentation:** [Initialize Chunked Upload](https://converthub.com/api/docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | body | `string` | yes | Original filename |
| `file_size` | body | `number` | yes | Total file size in bytes |
| `total_chunks` | body | `number` | yes | Number of chunks |
| `target_format` | body | `string` | yes | Target format for conversion |
| `webhook_url` | body | `string` | no | URL to receive webhook notification when complete |
| `options` | body | `object` | no | Conversion options |
| `metadata` | body | `object` | no | Custom metadata |
