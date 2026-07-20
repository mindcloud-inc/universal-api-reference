# List Check In Lists with pretix

Retrieves check-in lists from a pretix event.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizers/:organizer/events/:event/checkinlists/`
- **Base URL:** `https://pretix.eu/api/v1`
- **Official documentation:** [List Check In Lists](https://docs.pretix.eu/dev/api/resources/checkinlists.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizer` | path | `string` | yes | pretix organizer slug. |
| `event` | path | `string` | yes | pretix event slug. |
