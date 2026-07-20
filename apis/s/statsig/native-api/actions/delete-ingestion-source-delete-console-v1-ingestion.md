# Delete Ingestion Source with Statsig

Deletes an ingestion source from Statsig.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/console/v1/ingestion`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Delete Ingestion Source](https://docs.statsig.com/api-reference/ingestions/delete-ingestion-source)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `type` | query | `string` | yes |
| `dataset` | query | `string` | yes |
| `source_name` | query | `string` | no |
