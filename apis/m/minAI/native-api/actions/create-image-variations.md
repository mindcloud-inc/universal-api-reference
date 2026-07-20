# Create image variations with 1minAI

Creates image variations from an uploaded image in 1minAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/features`
- **Base URL:** `https://api.1min.ai`
- **Official documentation:** [Create image variations](https://docs.1min.ai/docs/api/ai-for-image/image-variator/flux-redux-schnell-image-variator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `imageUrl` | body | `string` | yes | — |
| `format` | body | `list` | no | Accepted values: `JPG`, `PNG`, `WebP`. |
| `aspectRatio` | body | `string` | no | — |
| `numOutputs` | body | `number` | no | — |
| `numInferenceSteps` | body | `number` | no | — |
| `outputQuality` | body | `number` | no | — |
| `megapixels` | body | `list` | no | Accepted values: `0.25 MP`, `1 MP`. |
