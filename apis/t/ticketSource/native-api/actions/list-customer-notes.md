# List Customer Notes with TicketSource

Retrieves notes for a customer from TicketSource.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers/{CustomerId}/notes`
- **Base URL:** `https://api.ticketsource.io`
- **Official documentation:** [List Customer Notes](https://www.ticketsource.io/working-with-customers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CustomerId` | path | `string` | yes | The unique identifier for a Customer record |
