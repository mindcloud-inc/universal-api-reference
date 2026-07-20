# Create Socialgist Reddit Job with Datastreamer

Creates a Socialgist Reddit job in Datastreamer.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/pipelines/:pipelineId/components/:componentId/jobs`
- **Base URL:** `https://api.platform.datastreamer.io`
- **Official documentation:** [Create Socialgist Reddit Job](https://docs.datastreamer.io/docs/socialgist-reddit)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `componentId` | path | `string` | no |
| `pipelineId` | path | `string` | no |
| `ready` | query | `string` | no |
