# Update Ticket Type with Checkout Page

Updates a ticket type in Checkout Page.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/events/:pageId/ticket-groups/:ticketGroupId/ticket-types/:ticketTypeId`
- **Base URL:** `https://api.checkoutpage.com`
- **Official documentation:** [Update Ticket Type](https://checkoutpage.com/docs/api/v1/events/ticket-groups/ticket-types/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageId` | path | `string` | yes | The unique identifier of the page. |
| `ticketGroupId` | path | `string` | yes | The unique identifier of the ticket group. |
| `ticketTypeId` | path | `string` | yes | The unique identifier of the ticket type. |
| `name` | body | `string` | no | Name of the ticket type. |
| `description` | body | `string` | no | Description of the ticket type. |
| `status` | body | `string` | no | Status of the ticket type. Defaults to `enabled`. |
| `price` | body | `number` | no | Price in smallest currency unit (cents). Defaults to `0`. |
| `reference` | body | `string` | no | External reference ID for the ticket type. |
| `hidden` | body | `boolean` | no | Whether the ticket type is hidden from customers. |
| `hideWhenSoldOut` | body | `boolean` | no | Hide the ticket type when sold out. |
| `hideWhenNotOnSale` | body | `boolean` | no | Hide the ticket type when not on sale. |
| `hideWhenScheduled` | body | `boolean` | no | Hide the ticket type when scheduled for future sale. |
| `hideWhenUnavailable` | body | `boolean` | no | Hide the ticket type when unavailable. |
| `pricing` | body | `string` | no | Pricing type for the ticket. Defaults to `paid`. |
| `discountedFromPrice` | body | `number` | no | Original price to show as discounted from (strike-through price). |
