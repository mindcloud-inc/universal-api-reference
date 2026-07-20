# Read Ingestion with Statsig

Retrieves an ingestion from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/ingestion`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Read Ingestion](https://docs.statsig.com/api-reference/ingestions/read-ingestion)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `type` | query | `string` | yes |
| `dataset` | query | `string` | yes |
| `source_name` | query | `string` | no |
