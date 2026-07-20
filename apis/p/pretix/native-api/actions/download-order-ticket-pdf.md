# Download Order Ticket PDF with pretix

Retrieves an order ticket PDF from pretix.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizers/:organizer/events/:event/orders/:code/download/pdf/`
- **Base URL:** `https://pretix.eu/api/v1`
- **Official documentation:** [Download Order Ticket PDF](https://docs.pretix.eu/dev/api/resources/orders.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizer` | path | `string` | yes | pretix organizer slug. |
| `event` | path | `string` | yes | pretix event slug. |
| `code` | path | `string` | yes | pretix order code. |
