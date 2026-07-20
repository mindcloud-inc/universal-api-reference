# Create Ticket with HappyFox

Creates a new ticket in HappyFox.

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets/`
- **Base URL:** `https://{accountDomain}/api/1.1/json`
- **Official documentation:** [Create Ticket](https://support.happyfox.com/kb/article/1039-tickets-endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Requester name. |
| `email` | body | `string` | yes | Requester email address. |
| `subject` | body | `string` | yes | Ticket subject. |
| `text` | body | `string` | yes | Ticket body in plain text. |
| `category` | body | `number` | yes | HappyFox category ID for the ticket. |
