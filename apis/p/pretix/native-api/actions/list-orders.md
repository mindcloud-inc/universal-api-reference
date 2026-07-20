# List Orders with pretix

Retrieves orders from a pretix event.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizers/:organizer/events/:event/orders/`
- **Base URL:** `https://pretix.eu/api/v1`
- **Official documentation:** [List Orders](https://docs.pretix.eu/dev/api/resources/orders.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Only return orders created with this email address. |
| `organizer` | path | `string` | yes | pretix organizer slug. |
| `search` | query | `string` | no | Search query for matching order names, emails, or companies. |
| `event` | path | `string` | yes | pretix event slug. |
