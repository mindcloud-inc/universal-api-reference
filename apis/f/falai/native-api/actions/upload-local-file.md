# Upload Local File with fal.ai

Creates a fal.ai storage file from a local upload.

## Endpoint

- **Method:** `POST`
- **Path:** `/serverless/files/file/local/:targetPath`
- **Base URL:** `https://api.fal.ai/v1`
- **Official documentation:** [Upload Local File](https://fal.ai/docs/api-reference/platform-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `targetPath` | path | `string` | yes | Destination file path in fal.ai serverless storage. |
