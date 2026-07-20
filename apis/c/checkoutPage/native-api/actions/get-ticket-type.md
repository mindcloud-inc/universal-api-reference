# Get Ticket Type with Checkout Page

Retrieves a ticket type from Checkout Page.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/events/:pageId/ticket-groups/:ticketGroupId/ticket-types/:ticketTypeId`
- **Base URL:** `https://api.checkoutpage.com`
- **Official documentation:** [Get Ticket Type](https://checkoutpage.com/docs/api/v1/events/ticket-groups/ticket-types/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageId` | path | `string` | yes | The unique identifier of the event page. |
| `ticketGroupId` | path | `string` | yes | The unique identifier of the ticket group. |
| `ticketTypeId` | path | `string` | yes | The unique identifier of the ticket type. |
