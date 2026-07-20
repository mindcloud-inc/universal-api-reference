# Get Inference Pipeline User with Openlayer

Retrieves a user for an inference pipeline in Openlayer.

## Endpoint

- **Method:** `GET`
- **Path:** `/inference-pipelines/:inferencePipelineId/user`
- **Base URL:** `https://api.openlayer.com/v1`
- **Official documentation:** [Get Inference Pipeline User](https://api.openlayer.com/v1/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inferencePipelineId` | path | `string` | yes | The inference pipeline ID. |
| `userId` | query | `string` | yes | The user ID to aggregate. |
