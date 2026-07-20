# List Pipeline Triggers with Statsig

Retrieves pipeline triggers from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/release_pipeline_triggers`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [List Pipeline Triggers](https://docs.statsig.com/api-reference/release-pipelines/list-pipeline-triggers)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `releasePipelineID` | query | `string` | no | Filter by Release Pipeline ID |
| `gateID` | query | `string` | no | Filter by Gate ID |
| `dynamicConfigID` | query | `string` | no | Filter by Dynamic Config ID |
| `status` | query | `string` | no | Filter by Status |
| `startDate` | query | `string` | no | Filter by the start date of the date range of the trigger's creation date in UTC, inclusive |
| `endDate` | query | `string` | no | Filter by the end date of the date range of the trigger's creation date in UTC, inclusive (i.e. until the end of the day); defaults to today's date if not provided |
| `limit` | query | `number` | no | Results per page |
| `page` | query | `number` | no | Page number |
