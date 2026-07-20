# Update Ticket Assignee with GrooveHQ

Updates a ticket's assignee in GrooveHQ.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tickets/:ticketNumber/assignee`
- **Base URL:** `https://api.groovehq.com/v1`
- **Official documentation:** [Update Ticket Assignee](https://doc.groovehq.com/tickets)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ticketNumber` | path | `string` | yes |
| `assignee` | body | `string` | yes |
| `skip_notifications` | body | `boolean` | no |
