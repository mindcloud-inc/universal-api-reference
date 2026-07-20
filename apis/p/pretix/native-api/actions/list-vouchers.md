# List Vouchers with pretix

Retrieves vouchers from a pretix event.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizers/:organizer/events/:event/vouchers/`
- **Base URL:** `https://pretix.eu/api/v1`
- **Official documentation:** [List Vouchers](https://docs.pretix.eu/dev/api/resources/vouchers.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizer` | path | `string` | yes | pretix organizer slug. |
| `event` | path | `string` | yes | pretix event slug. |
