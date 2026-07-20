# List Inference Pipeline User Sessions with Openlayer

## Endpoint

- **Method:** `GET`
- **Path:** `/inference-pipelines/:inferencePipelineId/user/sessions`
- **Base URL:** `https://api.openlayer.com/v1`
- **Official documentation:** [List Inference Pipeline User Sessions](https://api.openlayer.com/v1/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inferencePipelineId` | path | `string` | yes | The inference pipeline ID. |
| `userId` | query | `string` | yes | The user ID to list sessions for. |
