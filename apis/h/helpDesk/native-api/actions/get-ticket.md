# Get Ticket with HelpDesk

Retrieves a ticket from HelpDesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/tickets/:ticketID`
- **Base URL:** `https://api.helpdesk.com`
- **Official documentation:** [Get Ticket](https://api.helpdesk.com/docs#tag/Tickets/operation/ticketRead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketID` | path | `string` | yes | Unique HelpDesk ticket ID. |
