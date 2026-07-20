# Update Ticket with Request Tracker (RT)

Updates an existing ticket in Request Tracker.

## Endpoint

- **Method:** `PUT`
- **Path:** `ticket/:ticketId`
- **Base URL:** `https://try.requesttracker.io/sufongepl_57381/REST/2.0/`
- **Official documentation:** [Update Ticket](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Tickets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Owner` | body | `string` | no | Updated ticket owner user ID or username. |
| `Priority` | body | `number` | no | Updated RT ticket priority value. |
| `Queue` | body | `string` | no | Updated queue name or ID for the ticket. |
| `Status` | body | `string` | no | Updated RT ticket status. |
| `Subject` | body | `string` | no | Updated ticket subject. |
| `ticketId` | path | `string` | yes | The numeric RT ticket ID. |
