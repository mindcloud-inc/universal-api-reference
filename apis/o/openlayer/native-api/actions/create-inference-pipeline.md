# Create Inference Pipeline with Openlayer

Creates a new inference pipeline in Openlayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/inference-pipelines`
- **Base URL:** `https://api.openlayer.com/v1`
- **Official documentation:** [Create Inference Pipeline](https://api.openlayer.com/v1/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Inference pipeline description. |
| `name` | body | `string` | yes | Inference pipeline name. |
| `paused` | body | `boolean` | no | Whether the pipeline starts paused. |
| `projectId` | path | `string` | yes | Openlayer project ID. |
| `storageType` | body | `string` | yes | Pipeline storage type. |
