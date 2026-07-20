# Add Note To Ticket with Datalyse

Adds a note to a ticket in Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/tickets/addnote.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Add Note To Ticket](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Text of the note |
| `ticket_id` | body | `string` | yes | ID of the ticket |
