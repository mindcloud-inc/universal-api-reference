# Get Ticket Group with Checkout Page

Retrieves a ticket group from Checkout Page.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/events/:pageId/ticket-groups/:ticketGroupId`
- **Base URL:** `https://api.checkoutpage.com`
- **Official documentation:** [Get Ticket Group](https://checkoutpage.com/docs/api/v1/events/ticket-groups/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageId` | path | `string` | yes | The unique identifier of the event page. |
| `ticketGroupId` | path | `string` | yes | The unique identifier of the ticket group. |
