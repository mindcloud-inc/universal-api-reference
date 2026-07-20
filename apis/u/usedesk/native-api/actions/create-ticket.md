# Create Ticket with Usedesk

Creates a new ticket in Usedesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/create/ticket`
- **Base URL:** `https://secure.usedesk.com/uapi`
- **Official documentation:** [Create Ticket](https://api.usedocs.com/article/51378)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_email` | body | `string` | no | Client email when creating or attaching the ticket. |
| `client_name` | body | `string` | no | Client name when creating or attaching the ticket. |
| `priority` | body | `string` | no | Ticket priority: low, medium, urgent, or extreme. |
| `subject` | body | `string` | yes | Ticket subject. |
| `type` | body | `string` | no | Ticket type: question, task, problem, or incident. |
| `message` | body | `string` | yes | First ticket message. Supports HTML markup. |
| `client_id` | body | `number` | no | Client ID or the string new_client. |
| `channel_id` | body | `number` | no | Channel ID in which the ticket will be created. |
| `status` | body | `number` | no | Ticket status ID. |
