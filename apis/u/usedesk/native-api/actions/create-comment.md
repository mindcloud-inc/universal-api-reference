# Create Comment with Usedesk

Creates a new ticket comment in Usedesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/create/comment`
- **Base URL:** `https://secure.usedesk.com/uapi`
- **Official documentation:** [Create Comment](https://api.usedocs.com/article/51381)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | no | The side on whose behalf the comment is created: user or client. |
| `ticket_id` | body | `number` | yes | Ticket ID. |
| `type` | body | `string` | no | Comment type: public or private. |
| `message` | body | `string` | yes | Comment message. Supports HTML markup. |
| `user_id` | body | `number` | no | User ID on whose behalf the comment is created. |
