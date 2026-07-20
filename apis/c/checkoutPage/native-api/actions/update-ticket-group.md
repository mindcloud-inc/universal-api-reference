# Update Ticket Group with Checkout Page

Updates a ticket group in Checkout Page.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/events/:pageId/ticket-groups/:ticketGroupId`
- **Base URL:** `https://api.checkoutpage.com`
- **Official documentation:** [Update Ticket Group](https://checkoutpage.com/docs/api/v1/events/ticket-groups/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageId` | path | `string` | yes | The unique identifier of the page. |
| `ticketGroupId` | path | `string` | yes | The unique identifier of the ticket group. |
| `name` | body | `string` | no | Name of the ticket group. |
| `description` | body | `string` | no | Description of the ticket group. |
| `status` | body | `string` | no | Status of the ticket group. Defaults to `enabled`. |
| `reference` | body | `string` | no | External reference ID for the ticket group. |
| `layout` | body | `object` | no | Layout configuration for displaying ticket types. |
| `ticketSelectionType` | body | `string` | no | How customers can select tickets. Defaults to `quantity`. |
| `preselect` | body | `object` | no | Preselection configuration. |
| `capacity` | body | `number` | no | Maximum tickets that can be sold across all ticket types in this group. Omit or null for unlimited. |
| `hidden` | body | `boolean` | no | Whether the ticket group is hidden from customers. |
| `hideWhenSoldOut` | body | `boolean` | no | Hide the ticket group when all tickets are sold out. |
| `hideWhenNotOnSale` | body | `boolean` | no | Hide the ticket group when not on sale. |
| `hideWhenScheduled` | body | `boolean` | no | Hide the ticket group when scheduled for future sale. |
