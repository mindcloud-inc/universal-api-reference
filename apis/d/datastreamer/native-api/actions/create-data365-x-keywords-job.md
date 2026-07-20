# Create Data365 X Keywords Job with Datastreamer

Creates a Data365 X keyword search job in Datastreamer.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/pipelines/:pipelineId/components/:componentId/jobs`
- **Base URL:** `https://api.platform.datastreamer.io`
- **Official documentation:** [Create Data365 X Keywords Job](https://docs.datastreamer.io/docs/data365-x-keywords)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `componentId` | path | `string` | no |
| `data_source` | body | `string` | no |
| `from` | body | `string` | no |
| `job_name` | body | `string` | no |
| `job_type` | body | `string` | no |
| `pipelineId` | path | `string` | no |
| `query` | body | `object` | no |
| `ready` | query | `string` | no |
| `to` | body | `string` | no |
