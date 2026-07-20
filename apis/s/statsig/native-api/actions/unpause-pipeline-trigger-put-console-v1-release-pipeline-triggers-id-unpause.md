# Unpause Pipeline Trigger with Statsig

Unpauses a pipeline trigger in Statsig.

## Endpoint

- **Method:** `PUT`
- **Path:** `/console/v1/release_pipeline_triggers/{id}/unpause`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Unpause Pipeline Trigger](https://docs.statsig.com/api-reference/release-pipelines/unpause-pipeline-trigger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `phaseID` | body | `string` | yes | Request body field. |
