# Update Ticket with Intercom

## Endpoint

- **Method:** `PUT`
- **Path:** `/tickets/:ticket_id`
- **Base URL:** `https://api.intercom.io`
- **Official documentation:** [Update Ticket](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/tickets/updateticket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticket_id` | path | `string` | yes | Intercom ticket identifier |
| `ticket_state_id` | body | `string` | no | The ID of the ticket state associated with the ticket type |
| `company_id` | body | `string` | no | The ID of the company associated with the ticket |
| `open` | body | `boolean` | no | Whether the ticket is open |
| `is_shared` | body | `boolean` | no | Whether the ticket is visible to users |
| `snoozed_until` | body | `number` | no | Unix timestamp for when the ticket should reopen |
| `admin_id` | body | `number` | no | The ID of the admin performing the ticket update |
| `assignee_id` | body | `string` | no | The ID of the admin or team assigned to the ticket |
