# List Event Type Available Times with Calendly

Retrieves available times for a Calendly event type.

## Endpoint

- **Method:** `GET`
- **Path:** `/event_type_available_times`
- **Base URL:** `https://api.calendly.com`
- **Official documentation:** [List Event Type Available Times](https://developer.calendly.com/view-event-type-and-user-calendar-availability-data)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_type` | query | `list` | yes | Event type URI. Accepted values: `https://api.calendly.com/event_types/8d38b11a-269e-4878-ab4a-12048b63906d`. |
| `start_time` | query | `date` | yes | Start of interval (ISO-8601). |
| `end_time` | query | `date` | yes | End of interval (ISO-8601). |
