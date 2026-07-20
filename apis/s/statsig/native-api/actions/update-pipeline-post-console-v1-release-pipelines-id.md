# Update Pipeline with Statsig

Updates a pipeline in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/release_pipelines/{id}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Update Pipeline](https://docs.statsig.com/api-reference/release-pipelines/update-pipeline)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `name` | body | `string` | no | Request body field. |
| `phases` | body | `list` | no | Request body field. |
| `triggerNotice` | body | `string` | no | Request body field. |
