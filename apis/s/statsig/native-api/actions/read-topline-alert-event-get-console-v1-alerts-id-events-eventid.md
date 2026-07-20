# Read Topline Alert Event with Statsig

Retrieves a topline alert event from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/alerts/{id}/events/{eventId}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Read Topline Alert Event](https://docs.statsig.com/api-reference/alerts/read-topline-alert-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `eventId` | path | `string` | yes | alert event id |
