# Edit Image with Claid AI

Creates an edited image in Claid AI.

## Endpoint

- **Method:** `POST`
- **Path:** `image/edit`
- **Base URL:** `https://api.claid.ai/v1`
- **Official documentation:** [Edit Image](https://docs.claid.ai/image-editing-api/api-reference)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `input` | body | `string` | yes |
| `operations` | body | `object` | yes |
| `output` | body | `string` | no |
