# Get Order Position with pretix

Retrieves an order position from pretix.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizers/:organizer/events/:event/orderpositions/:position/`
- **Base URL:** `https://pretix.eu/api/v1`
- **Official documentation:** [Get Order Position](https://docs.pretix.eu/dev/api/resources/orders.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizer` | path | `string` | yes | pretix organizer slug. |
| `event` | path | `string` | yes | pretix event slug. |
| `position` | path | `string` | yes | pretix order position ID. |
