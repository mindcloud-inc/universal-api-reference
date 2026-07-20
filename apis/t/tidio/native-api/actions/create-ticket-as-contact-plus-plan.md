# Create Ticket (As Contact) [Plus plan] with Tidio

Creates a ticket as a contact in Tidio.

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets/as-contact`
- **Base URL:** `https://api.tidio.com`
- **Official documentation:** [Create Ticket (As Contact) [Plus plan]](https://developers.tidio.com/reference/post_tickets-as-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_email` | body | `string` | yes | Email address of the contact creating the ticket. |
| `subject` | body | `string` | yes | Subject line of the ticket. |
| `message_content` | body | `string` | yes | Initial message body for the ticket. |
| `assigned_department_id` | body | `string` | no | Optional department UUID to assign the ticket to. |
| `custom_channel_id` | body | `string` | no | Optional custom channel identifier used for the ticket source. |
