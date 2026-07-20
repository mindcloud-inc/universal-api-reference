# Edit Ticket with Datalyse

Updates an existing ticket in Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/tickets/edit.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Edit Ticket](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | body | `string` | no | Agent ID or "unassigned" (optional) |
| `pipeline` | body | `string` | no | Pipeline ID (optional) |
| `status` | body | `string` | no | Status ID (optional) |
| `ticket_id` | body | `string` | yes | ID of the ticket to edit |
| `ticketdescription` | body | `string` | no | Description for the ticket (optional) |
| `ticketname` | body | `string` | no | Name for the ticket (optional) |
