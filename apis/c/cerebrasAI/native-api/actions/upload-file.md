# Upload File with Cerebras AI

Creates a file in Cerebras AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/files`
- **Base URL:** `https://api.cerebras.ai`
- **Official documentation:** [Upload File](https://inference-docs.cerebras.ai/api-reference/file/upload-file)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
| `purpose` | body | `string` | yes |
