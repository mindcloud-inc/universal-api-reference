# Update Model with Airiam AI

Updates an existing model in Airiam AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/models/:modelId`
- **Base URL:** `https://platform.sectorflow.ai`
- **Official documentation:** [Update Model](https://docs.ai.airiam.com/reference/models)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modelId` | path | `string` | yes | Model UUID. |
| `name` | body | `string` | no | Updated model display name. |
