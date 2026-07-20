# Create Reply with Freshdesk

Creates a reply to a Freshdesk ticket.

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets/:id/reply`
- **Base URL:** `https://{subdomain}.freshdesk.com/api/v2`
- **Official documentation:** [Create Reply](https://developers.freshdesk.com/api/#reply_ticket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `list<number>` | yes | Freshdesk ticket ID. |
| `body` | body | `string` | no | Reply content in HTML |
| `structured_body` | body | `object` | no | Structured content body for the reply |
| `attachments[]` | body | `array<object>` | no | Reply attachments |
| `from_email` | body | `string` | no | Email address from which the reply is sent |
| `user_id` | body | `list<number>` | no | Agent user ID adding the reply |
| `cc_emails[]` | body | `array<string>` | no | CC recipients for the outgoing reply |
| `bcc_emails[]` | body | `array<string>` | no | BCC recipients for the outgoing reply |
