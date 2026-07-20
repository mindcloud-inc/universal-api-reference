# List Events with pretix

Retrieves events from a pretix organizer.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizers/:organizer/events/`
- **Base URL:** `https://pretix.eu/api/v1`
- **Official documentation:** [List Events](https://docs.pretix.eu/dev/api/resources/events.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizer` | path | `string` | yes | pretix organizer slug. |
