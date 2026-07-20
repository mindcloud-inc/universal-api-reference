# Create DarkOwl Search Job with Datastreamer

Creates a DarkOwl search job in Datastreamer.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/pipelines/:pipelineId/components/:componentId/jobs`
- **Base URL:** `https://api.platform.datastreamer.io`
- **Official documentation:** [Create DarkOwl Search Job](https://docs.datastreamer.io/docs/darkowl-search)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `componentId` | path | `string` | no |
| `pipelineId` | path | `string` | no |
| `ready` | query | `string` | no |
