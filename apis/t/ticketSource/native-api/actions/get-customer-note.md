# Get Customer Note with TicketSource

Retrieves a customer note from TicketSource.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers/{CustomerId}/notes/{CustomerNoteId}`
- **Base URL:** `https://api.ticketsource.io`
- **Official documentation:** [Get Customer Note](https://www.ticketsource.io/working-with-customers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CustomerId` | path | `string` | yes | The unique identifier for a Customer record |
| `CustomerNoteId` | path | `string` | yes | The unique identifier for a Customer Note record |
