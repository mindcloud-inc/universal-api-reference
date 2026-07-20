# List Sub Events with pretix

Retrieves sub-events from a pretix event.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizers/:organizer/events/:event/subevents/`
- **Base URL:** `https://pretix.eu/api/v1`
- **Official documentation:** [List Sub Events](https://docs.pretix.eu/dev/api/resources/subevents.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizer` | path | `string` | yes | pretix organizer slug. |
| `event` | path | `string` | yes | pretix event slug. |
