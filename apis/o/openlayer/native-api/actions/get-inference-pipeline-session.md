# Get Inference Pipeline Session with Openlayer

Retrieves a session for an inference pipeline in Openlayer.

## Endpoint

- **Method:** `GET`
- **Path:** `/inference-pipelines/:inferencePipelineId/session`
- **Base URL:** `https://api.openlayer.com/v1`
- **Official documentation:** [Get Inference Pipeline Session](https://api.openlayer.com/v1/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inferencePipelineId` | path | `string` | yes | The inference pipeline ID. |
| `sessionId` | query | `string` | yes | The session ID to aggregate. |
