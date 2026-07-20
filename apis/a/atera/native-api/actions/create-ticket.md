# Create ticket with Atera

Creates a ticket in Atera.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/tickets`
- **Base URL:** `https://app.atera.com`
- **Official documentation:** [Create ticket](https://app.atera.com/apidocs#!/Ticket/Ticket_Post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Description` | body | `string` | yes | Ticket description. |
| `EndUserEmail` | body | `string` | no | New end user email. |
| `EndUserFirstName` | body | `string` | no | New end user first name. |
| `EndUserID` | body | `number` | no | Existing end user contact ID. |
| `EndUserLastName` | body | `string` | no | New end user last name. |
| `EndUserPhone` | body | `string` | no | New end user phone. |
| `TechnicianContactID` | body | `number` | no | Technician contact ID. |
| `TechnicianEmail` | body | `string` | no | Technician email. |
| `TicketImpact` | body | `string` | no | Ticket impact. |
| `TicketPriority` | body | `string` | no | Ticket priority. |
| `TicketStatus` | body | `string` | no | Ticket status. |
| `TicketTitle` | body | `string` | yes | Ticket title. |
| `TicketType` | body | `string` | no | Ticket type. |
