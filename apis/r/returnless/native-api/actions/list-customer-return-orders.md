# List Customer Return Orders with Returnless

Retrieves customer return orders from Returnless.

## Endpoint

- **Method:** `GET`
- **Path:** `/2025-01/customers/{customer}/return-orders`
- **Base URL:** `https://api-v2.returnless.com`
- **Official documentation:** [List Customer Return Orders](https://docs.returnless.com/docs/api-rest-reference/ed737183af993)

## Capabilities

This operation supports [filtering](../README.md#filtering) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer` | path | `string` | yes | The unique identifier of the customer. |
