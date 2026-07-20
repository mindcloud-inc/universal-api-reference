# Change Ticket Mailbox with GrooveHQ

Changes a ticket's mailbox in GrooveHQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets/:ticketId/change_mailbox/:mailboxId`
- **Base URL:** `https://api.groovehq.com/v1`
- **Official documentation:** [Change Ticket Mailbox](https://doc.groovehq.com/tickets)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ticketId` | path | `string` | yes |
| `mailboxId` | path | `string` | yes |
