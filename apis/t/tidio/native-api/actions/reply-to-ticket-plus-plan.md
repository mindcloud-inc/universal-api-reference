# Reply to Ticket [Plus plan] with Tidio

Replies to a ticket in the Tidio workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets/{ticketId}/reply`
- **Base URL:** `https://api.tidio.com`
- **Official documentation:** [Reply to Ticket [Plus plan]](https://developers.tidio.com/reference/post_tickets-ticketid-reply)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | path | `string` | yes | The Tidio ticket ID. |
| `author_type` | body | `string` | yes | Reply author type. |
| `content` | body | `string` | yes | Reply message content. |
| `operator_id` | body | `string` | no | Operator UUID when the reply author type is operator. |
| `message_type` | body | `string` | no | Reply visibility type. |
