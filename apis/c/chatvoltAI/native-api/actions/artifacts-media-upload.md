# Upload Media with Chatvolt AI

Uploads media to Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/artifacts/media/upload`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Upload Media](https://docs.chatvolt.ai/api-reference/endpoint/artifacts/media/upload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `string` | yes | File for multipart/form-data requests. |
| `artifact_id` | body | `string` | yes | Artifact Id for multipart/form-data requests. |
| `name` | body | `string` | yes | Name for multipart/form-data requests. |
| `alt_description` | body | `string` | no | Alt Description for multipart/form-data requests. |
