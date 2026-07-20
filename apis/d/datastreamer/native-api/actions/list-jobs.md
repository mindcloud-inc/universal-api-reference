# List Jobs with Datastreamer

Retrieves previously created jobs from Datastreamer.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/pipelines/:pipelineId/components/:componentId/jobs`
- **Base URL:** `https://api.platform.datastreamer.io`
- **Official documentation:** [List Jobs](https://docs.datastreamer.io/docs/listing-jobs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `pipelineId` | path | `string` | yes |
| `componentId` | path | `string` | yes |
| `count` | query | `number` | no |
