# Backfill Ingestion with Statsig

Backfills an ingestion in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/ingestion/backfill`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Backfill Ingestion](https://docs.statsig.com/api-reference/ingestions/backfill-ingestion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datestamp_start` | body | `string` | yes | Request body field. |
| `datestamp_end` | body | `string` | yes | Request body field. |
| `type` | body | `string` | yes | Request body field. |
| `source` | body | `string` | no | Request body field. |
| `dataset` | body | `string` | yes | Request body field. |
