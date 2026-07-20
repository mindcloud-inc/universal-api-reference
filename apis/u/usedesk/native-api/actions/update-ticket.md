# Update Ticket with Usedesk

Updates an existing ticket in Usedesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/update/ticket`
- **Base URL:** `https://secure.usedesk.com/uapi`
- **Official documentation:** [Update Ticket](https://api.usedocs.com/article/51379)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `priority` | body | `string` | no | Ticket priority: low, medium, urgent, or extreme. |
| `silent` | body | `string` | no | Disable the automatic status change when true or 1. |
| `subject` | body | `string` | no | Ticket subject. |
| `tag` | body | `string` | no | Tags separated by comma and space. |
| `ticket_id` | body | `number` | yes | Ticket ID. |
| `type` | body | `string` | no | Ticket type: question, task, problem, or incident. |
| `client_id` | body | `number` | no | Client ID. |
| `group_id` | body | `number` | no | Group ID. |
| `assignee_id` | body | `number` | no | Assignee user ID. |
| `user_id` | body | `number` | no | User ID on whose behalf the changes will be made. |
| `status` | body | `number` | no | Ticket status ID. |
