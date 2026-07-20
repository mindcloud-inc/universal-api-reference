# Approve Pipeline Trigger Phase with Statsig

Approves a pipeline trigger phase in Statsig.

## Endpoint

- **Method:** `PUT`
- **Path:** `/console/v1/release_pipeline_triggers/{id}/approve`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Approve Pipeline Trigger Phase](https://docs.statsig.com/api-reference/release-pipelines/approve-pipeline-trigger-phase)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `phaseID` | body | `string` | yes | Request body field. |
