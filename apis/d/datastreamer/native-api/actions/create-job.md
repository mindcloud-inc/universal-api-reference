# Create Job with Datastreamer

Creates a new job in Datastreamer.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/pipelines/:pipelineId/components/:componentId/jobs`
- **Base URL:** `https://api.platform.datastreamer.io`
- **Official documentation:** [Create Job](https://docs.datastreamer.io/docs/creating-jobs-portal-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipelineId` | path | `string` | yes | — |
| `componentId` | path | `string` | yes | — |
| `ready` | query | `boolean` | no | — |
| `job_name` | body | `string` | yes | Job name to persist on the created job. |
| `data_source` | body | `string` | yes | Datastreamer data source for the job. |
| `query` | body | `object` | yes | Full query object for the created job payload. |
| `job_type` | body | `string` | yes | Job type, for example periodic. |
| `schedule` | body | `string` | yes | Cron schedule for a periodic job. |
| `label` | body | `string` | no | Optional label applied to job output. |
