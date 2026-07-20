# Create WebSightLine Threads Job with Datastreamer

Creates a WebSightLine Threads job in Datastreamer.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/pipelines/:pipelineId/components/:componentId/jobs`
- **Base URL:** `https://api.platform.datastreamer.io`
- **Official documentation:** [Create WebSightLine Threads Job](https://docs.datastreamer.io/docs/websightline-threads)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `componentId` | path | `string` | no |
| `pipelineId` | path | `string` | no |
| `ready` | query | `string` | no |
