# Create Customer Note with TicketSource

Creates a new customer note in TicketSource.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/{CustomerId}/notes`
- **Base URL:** `https://api.ticketsource.io`
- **Official documentation:** [Create Customer Note](https://www.ticketsource.io/working-with-customers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CustomerId` | path | `string` | yes | The unique identifier for a Customer record |
| `data` | body | `object` | no | A Customer Note against a specific Customer record. |
