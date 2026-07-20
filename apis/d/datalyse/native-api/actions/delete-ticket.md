# Delete Ticket with Datalyse

Deletes an existing ticket from Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/tickets/delete.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Delete Ticket](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticket_id` | body | `string` | yes | ID of the ticket to delete |
