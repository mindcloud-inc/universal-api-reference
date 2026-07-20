# Update ticket with Atera

Updates an existing ticket in Atera.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v3/tickets/:ticketId`
- **Base URL:** `https://app.atera.com`
- **Official documentation:** [Update ticket](https://app.atera.com/apidocs#!/Ticket/Ticket_Put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TechnicianContactID` | body | `number` | no | Technician contact ID. |
| `TechnicianEmail` | body | `string` | no | Technician email. |
| `ticketId` | path | `number` | yes | System ticket ID. |
| `TicketImpact` | body | `string` | no | Ticket impact. |
| `TicketPriority` | body | `string` | no | Ticket priority. |
| `TicketStatus` | body | `string` | no | Ticket status. |
| `TicketTitle` | body | `string` | no | Ticket title. |
| `TicketType` | body | `string` | no | Ticket type. |
