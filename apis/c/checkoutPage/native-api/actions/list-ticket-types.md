# List Ticket Types with Checkout Page

Retrieves ticket types from Checkout Page.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/events/:pageId/ticket-groups/:ticketGroupId/ticket-types`
- **Base URL:** `https://api.checkoutpage.com`
- **Official documentation:** [List Ticket Types](https://checkoutpage.com/docs/api/v1/events/ticket-groups/ticket-types/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageId` | path | `string` | yes | The unique identifier of the event page. |
| `ticketGroupId` | path | `string` | yes | The unique identifier of the ticket group. |
