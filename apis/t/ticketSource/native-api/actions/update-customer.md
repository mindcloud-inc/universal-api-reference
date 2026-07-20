# Update Customer with TicketSource

Updates an existing customer in TicketSource.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/customers/{CustomerId}`
- **Base URL:** `https://api.ticketsource.io`
- **Official documentation:** [Update Customer](https://www.ticketsource.io/working-with-customers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CustomerId` | path | `string` | yes | The unique identifier for a Customer record |
| `data` | body | `object` | no | Customer fields to update. |
