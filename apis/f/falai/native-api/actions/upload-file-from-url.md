# Upload File From URL with fal.ai

Creates a fal.ai storage file from a URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/serverless/files/file/url/:file`
- **Base URL:** `https://api.fal.ai/v1`
- **Official documentation:** [Upload File From URL](https://fal.ai/docs/api-reference/platform-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | path | `string` | yes | Destination file path in fal.ai serverless storage. |
| `url` | body | `string` | yes | Public URL of the file to import. |
