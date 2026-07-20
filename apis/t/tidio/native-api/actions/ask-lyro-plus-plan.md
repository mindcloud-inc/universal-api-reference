# Ask Lyro [Plus plan] with Tidio

Asks Lyro to answer a ticket in Tidio.

## Endpoint

- **Method:** `POST`
- **Path:** `/lyro/tickets`
- **Base URL:** `https://api.tidio.com`
- **Official documentation:** [Ask Lyro [Plus plan]](https://developers.tidio.com/reference/post_lyro-tickets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticket_id` | body | `string` | yes | Tidio ticket identifier to answer with Lyro. |
| `subject` | body | `string` | yes | Ticket subject shown to Lyro. |
| `contact_email` | body | `string` | yes | Email address of the contact tied to the ticket. |
| `contact_name` | body | `string` | yes | Display name of the contact tied to the ticket. |
| `recipient_email` | body | `string` | yes | Recipient email where the Lyro answer will be sent. |
| `messages` | body | `list<object>` | yes | Conversation messages used as Lyro context. |
| `messages[].created_at` | body | `date` | yes | Message creation timestamp in ISO 8601 format. |
| `messages[].message_id` | body | `string` | yes | Unique ULID of the conversation message. |
| `messages[].author_type` | body | `string` | yes | Message author type. Tidio currently accepts contact only. |
| `messages[].message_type` | body | `string` | yes | Message visibility type. Tidio currently accepts public only. |
| `messages[].attachments` | body | `list<string>` | no | Optional attachment URLs for the message. |
| `messages[].message_content` | body | `string` | yes | Body text of the conversation message. |
