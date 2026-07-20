# Create Pipeline with Statsig

Creates a pipeline in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/release_pipelines`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Create Pipeline](https://docs.statsig.com/api-reference/release-pipelines/create-pipeline)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Request body field. |
| `phases` | body | `list` | no | Request body field. |
| `triggerNotice` | body | `string` | no | Request body field. |
