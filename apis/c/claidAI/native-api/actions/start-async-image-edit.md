# Start Async Image Edit with Claid AI

Starts an asynchronous image edit in Claid AI.

## Endpoint

- **Method:** `POST`
- **Path:** `image/edit/async`
- **Base URL:** `https://api.claid.ai/v1`
- **Official documentation:** [Start Async Image Edit](https://docs.claid.ai/image-editing-api/async-api-reference)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `input` | body | `string` | yes |
| `operations` | body | `object` | yes |
| `output` | body | `string` | no |
