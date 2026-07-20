# List Directory Files with fal.ai

Retrieves storage files from a fal.ai directory.

## Endpoint

- **Method:** `GET`
- **Path:** `/serverless/files/list/:dir`
- **Base URL:** `https://api.fal.ai/v1`
- **Official documentation:** [List Directory Files](https://fal.ai/docs/api-reference/platform-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dir` | path | `string` | yes | Serverless directory path to list. |
