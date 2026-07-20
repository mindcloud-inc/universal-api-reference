# Create Ticket with Moxie

Creates a new ticket in Moxie.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/tickets/create`
- **Base URL:** `https://pod01.withmoxie.com/api/public`
- **Official documentation:** [Create Ticket](https://help.withmoxie.com/en/articles/9367715-create-ticket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userEmail` | body | `string` | yes | Email of the user creating the ticket. |
| `ticketType` | body | `string` | yes | Ticket type identifier. |
| `subject` | body | `string` | yes | Ticket subject line. |
| `comment` | body | `string` | yes | Initial ticket comment body. |
| `dueDate` | body | `date` | no | Ticket due date. |
| `formData` | body | `object` | no | Ticket form data object. |
