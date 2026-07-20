# Get Processing Status with EyeLevel.ai

Retrieves an ingest process status from EyeLevel.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/ingest/:processId`
- **Base URL:** `https://api.groundx.ai/api/v1`
- **Official documentation:** [Get Processing Status](https://docs.eyelevel.ai/reference/api-reference/documents/get-processing-status-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `processId` | path | `string` | yes | The processId of the ingest job to inspect. |
