# Generate AI Photos with Apiframe

Creates an AI photo generation task in Apiframe.

## Endpoint

- **Method:** `POST`
- **Path:** `/ai-photo-generate`
- **Base URL:** `https://api.apiframe.pro`
- **Official documentation:** [Generate AI Photos](https://docs.apiframe.ai/ai-photos/generate)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `training_id` | body | `string` | yes |
| `prompt` | body | `string` | yes |
