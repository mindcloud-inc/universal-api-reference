# Update Ticket Group with GrooveHQ

Updates a ticket's assigned group in GrooveHQ.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tickets/:ticketNumber/assigned_group`
- **Base URL:** `https://api.groovehq.com/v1`
- **Official documentation:** [Update Ticket Group](https://doc.groovehq.com/tickets)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ticketNumber` | path | `string` | yes |
| `group` | body | `string` | yes |
| `skip_notifications` | body | `boolean` | no |
