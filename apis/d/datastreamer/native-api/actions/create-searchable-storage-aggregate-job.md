# Create Searchable Storage Aggregate Job with Datastreamer

Creates a Searchable Storage aggregate job in Datastreamer.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/pipelines/:pipelineId/components/:componentId/jobs`
- **Base URL:** `https://api.platform.datastreamer.io`
- **Official documentation:** [Create Searchable Storage Aggregate Job](https://docs.datastreamer.io/docs/searchable-storage-ingress)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `componentId` | path | `string` | no |
| `pipelineId` | path | `string` | no |
| `ready` | query | `string` | no |
