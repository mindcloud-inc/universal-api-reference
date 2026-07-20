# Process Batch Image Edit with Claid AI

Starts a batch image edit in Claid AI.

## Endpoint

- **Method:** `POST`
- **Path:** `image/edit/batch`
- **Base URL:** `https://api.claid.ai/v1`
- **Official documentation:** [Process Batch Image Edit](https://docs.claid.ai/image-editing-api/batch-api-reference)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `input` | body | `object` | yes |
| `operations` | body | `object` | yes |
| `output` | body | `string` | no |
