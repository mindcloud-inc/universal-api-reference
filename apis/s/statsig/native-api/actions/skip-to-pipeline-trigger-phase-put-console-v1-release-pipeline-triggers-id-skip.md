# Skip to Pipeline Trigger Phase with Statsig

Skips to a pipeline trigger phase in Statsig.

## Endpoint

- **Method:** `PUT`
- **Path:** `/console/v1/release_pipeline_triggers/{id}/skip`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Skip to Pipeline Trigger Phase](https://docs.statsig.com/api-reference/release-pipelines/skip-to-pipeline-trigger-phase)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `phaseID` | body | `string` | yes | Request body field. |
