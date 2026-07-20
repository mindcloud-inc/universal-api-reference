# List Order Positions with pretix

Retrieves order positions from a pretix event.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizers/:organizer/events/:event/orderpositions/`
- **Base URL:** `https://pretix.eu/api/v1`
- **Official documentation:** [List Order Positions](https://docs.pretix.eu/dev/api/resources/orders.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order` | query | `string` | no | Optional order code filter for order positions. |
| `organizer` | path | `string` | yes | pretix organizer slug. |
| `event` | path | `string` | yes | pretix event slug. |
