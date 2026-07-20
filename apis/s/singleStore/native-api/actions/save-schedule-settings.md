# Save Schedule Settings with SingleStore

Updates schedule settings in SingleStore.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/config-sched`
- **Base URL:** `https://{flowEndpoint}:30081/ingest/api/ingest`
- **Official documentation:** [Save Schedule Settings](https://docs.singlestore.com/cloud/load-data/load-data-with-singlestore-flow-on-helios/flow-on-helios-api/flow-on-helios-ingest-api/#save-schedule-settings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Scheduling mode to save for ingest runs. |
| `duration` | body | `string` | no | Schedule interval duration value. |
| `offset` | body | `string` | no | Offset to apply to the saved schedule. |
| `weekFlags` | body | `string` | no | Days of the week in YYYYYYY format, from Sunday through Saturday, when the schedule type is weekly. |
