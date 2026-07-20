# Download with Vectorizer AI

## Endpoint

- **Method:** `POST`
- **Path:** `/download`
- **Base URL:** `https://api.vectorizer.ai/api/v1`
- **Official documentation:** [Download](https://vectorizer.ai/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image.token` | body | `string` | no | — |
| `receipt` | body | `string` | no | — |
| `output.file_format` | body | `list` | no | Accepted values: `dxf`, `eps`, `pdf`, `png`, `svg`. |
