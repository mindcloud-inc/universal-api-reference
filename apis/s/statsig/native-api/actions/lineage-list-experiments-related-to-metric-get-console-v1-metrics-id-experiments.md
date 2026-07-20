# Lineage: List experiments related to Metric with Statsig

Retrieves experiments related to a Statsig metric.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/metrics/{id}/experiments`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Lineage: List experiments related to Metric](https://docs.statsig.com/api-reference/metrics/lineage-list-experiments-related-to-metric)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `layerID` | query | `string` | no | Which layer to place the experiment into. |
| `idType` | query | `string` | no | The idType the experiment will be performed on |
| `teamID` | query | `string` | no | The team ID associated with the experiment, Enterprise only. |
| `status` | query | `string` | no | The current status of the experiment |
| `targetAppID` | query | `string` | no | — |
| `stale` | query | `boolean` | no | When true, only returns stale experiments. If omitted or false, returns all experiments. |
| `createdStartDate` | query | `string` | no | Expected valid date in the form of YYYY-MM-DD |
| `createdEndDate` | query | `string` | no | Expected valid date in the form of YYYY-MM-DD |
| `experimentType` | query | `string` | no | Filter by experiment type |
| `creatorName` | query | `string` | no | Name of the creator. |
| `creatorID` | query | `string` | no | ID of the user who created the entity. |
| `tags` | query | `string` | no | Filter by tags |
| `limit` | query | `number` | no | Results per page |
| `page` | query | `number` | no | Page number |
