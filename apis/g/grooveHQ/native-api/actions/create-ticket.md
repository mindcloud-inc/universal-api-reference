# Create Ticket with GrooveHQ

Creates a new ticket in GrooveHQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets`
- **Base URL:** `https://api.groovehq.com/v1`
- **Official documentation:** [Create Ticket](https://doc.groovehq.com/tickets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | yes | — |
| `from` | body | `string` | yes | — |
| `to` | body | `string` | yes | — |
| `mailbox` | body | `string` | no | — |
| `assigned_group` | body | `string` | no | — |
| `assignee` | body | `string` | no | — |
| `note` | body | `boolean` | no | — |
| `send_copy_to_customer` | body | `boolean` | no | — |
| `state` | body | `string` | no | — |
| `subject` | body | `string` | no | — |
| `tags[]` | body | `array<string>` | no | Send multiple values as a array. |
| `tags[]` | body | `array<string>` | no | Send multiple values as a array. |
| `starred` | body | `boolean` | no | — |
| `skip_notifications` | body | `boolean` | no | — |
