# Create Bluesky Live Feed Job with Datastreamer

Creates a Bluesky live feed job in Datastreamer.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/pipelines/:pipelineId/components/:componentId/jobs`
- **Base URL:** `https://api.platform.datastreamer.io`
- **Official documentation:** [Create Bluesky Live Feed Job](https://docs.datastreamer.io/docs/bluesky-live-feed)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `componentId` | path | `string` | no |
| `pipelineId` | path | `string` | no |
| `ready` | query | `string` | no |
