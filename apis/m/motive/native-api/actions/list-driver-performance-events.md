# List driver performance events with Motive

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/driver_performance_events`
- **Base URL:** `https://api.gomotive.com`
- **Official documentation:** [List driver performance events](https://developer-docs.gomotive.com/reference/fetch-all-the-drivers-performance-events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driver_ids` | query | `list<number>` | no | Filter events by one or more driver IDs. Send multiple values as a array. |
| `vehicle_ids` | query | `list<number>` | no | Filter events by one or more vehicle IDs. Send multiple values as a array. |
| `event_types` | query | `list<string>` | no | Filter events by Motive event type. Send multiple values as a array. |
| `start_date` | query | `date` | no | Fetch events from this date onward. |
| `end_date` | query | `date` | no | Fetch events up to this date. |
| `updated_after` | query | `date` | no | Return events updated after the given timestamp. |
