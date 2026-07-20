# Delete Customer Note with TicketSource

Deletes an existing customer note from TicketSource.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/customers/{CustomerId}/notes/{CustomerNoteId}`
- **Base URL:** `https://api.ticketsource.io`
- **Official documentation:** [Delete Customer Note](https://www.ticketsource.io/working-with-customers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CustomerId` | path | `string` | yes | The unique identifier for a Customer record |
| `CustomerNoteId` | path | `string` | yes | The unique identifier for a Customer Note record |
