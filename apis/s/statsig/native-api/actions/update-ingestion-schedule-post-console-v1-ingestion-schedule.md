# Update Ingestion Schedule with Statsig

Updates an ingestion schedule in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/ingestion/schedule`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Update Ingestion Schedule](https://docs.statsig.com/api-reference/ingestions/update-ingestion-schedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | body | `string` | yes | Request body field. |
| `scheduled_hour_pst` | body | `number` | no | Request body field. |
