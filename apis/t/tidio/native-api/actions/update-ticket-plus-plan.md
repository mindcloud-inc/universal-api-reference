# Update Ticket [Plus plan] with Tidio

Updates a ticket in the Tidio workspace.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tickets/{ticketId}`
- **Base URL:** `https://api.tidio.com`
- **Official documentation:** [Update Ticket [Plus plan]](https://developers.tidio.com/reference/patch_tickets-ticketid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | path | `string` | yes | The Tidio ticket ID. |
| `status` | body | `string` | no | Updated ticket status. |
| `priority` | body | `string` | no | Updated ticket priority. |
| `assigned.type` | body | `string` | no | Assignment target type: department or operator. |
| `assigned.id` | body | `string` | no | UUID of the assigned department or operator. |
