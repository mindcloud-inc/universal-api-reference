# Update Ticket State with GrooveHQ

Updates a ticket's state in GrooveHQ.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tickets/:ticketNumber/state`
- **Base URL:** `https://api.groovehq.com/v1`
- **Official documentation:** [Update Ticket State](https://doc.groovehq.com/tickets)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ticketNumber` | path | `string` | yes |
| `state` | body | `string` | yes |
