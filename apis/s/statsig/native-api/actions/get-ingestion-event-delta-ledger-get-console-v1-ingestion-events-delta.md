# Get Ingestion Event Delta Ledger with Statsig

Retrieves an ingestion event delta ledger from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/ingestion/events/delta`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Get Ingestion Event Delta Ledger](https://docs.statsig.com/api-reference/ingestions/get-ingestion-event-delta-ledger)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_name` | query | `string` | no | — |
| `event_name` | query | `string` | no | — |
| `start_date` | query | `string` | yes | Expected valid date in the form of YYYY-MM-DD |
| `end_date` | query | `string` | yes | Expected valid date in the form of YYYY-MM-DD |
