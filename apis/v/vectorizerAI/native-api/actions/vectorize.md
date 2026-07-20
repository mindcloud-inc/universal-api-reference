# Vectorize with Vectorizer AI

## Endpoint

- **Method:** `POST`
- **Path:** `/vectorize`
- **Base URL:** `https://api.vectorizer.ai/api/v1`
- **Official documentation:** [Vectorize](https://vectorizer.ai/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | no | — |
| `mode` | body | `list` | no | Accepted values: `preview`, `production`, `test`, `test_preview`. |
| `input.max_pixels` | body | `number` | no | — |
| `processing.max_colors` | body | `number` | no | — |
| `processing.palette` | body | `string` | no | — |
| `policy.retention_days` | body | `number` | no | — |
| `image.url` | body | `string` | no | — |
| `image.base64` | body | `string` | no | — |
| `image.token` | body | `string` | no | — |
