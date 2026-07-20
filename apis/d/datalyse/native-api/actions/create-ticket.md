# Create Ticket with Datalyse

Creates a new ticket in Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/tickets/create.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Create Ticket](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | body | `string` | no | Set to "unassigned" to assign this ticket to all agents, or provide a specific agent_id (optional) |
| `lead_id` | body | `string` | yes | ID of the contact or company |
| `pipeline` | body | `string` | no | Pipeline ID (optional) |
| `status` | body | `string` | no | Status ID |
| `ticketdescription` | body | `string` | yes | Description for the ticket |
| `ticketname` | body | `string` | yes | Name for the ticket |
| `ticketvisiblecabinet` | body | `string` | no | Visible in client cabinet (optional) |
