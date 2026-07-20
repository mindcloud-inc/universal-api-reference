# List Event Attendees with Billetto

Retrieves attendees for an event from Billetto.

## Endpoint

- **Method:** `GET`
- **Path:** `organiser/events/{id}/attendees`
- **Base URL:** `https://billetto.dk/api/v3`
- **Official documentation:** [List Event Attendees](https://api.billetto.com/reference/list-attendees-on-a-specific-event-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Billetto event ID. |
