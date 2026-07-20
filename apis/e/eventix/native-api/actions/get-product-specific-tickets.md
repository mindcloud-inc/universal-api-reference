# Get Ticket Types of Product Type with Eventix

Retrieves ticket types for an Eventix product type.

## Endpoint

- **Method:** `GET`
- **Path:** `/3.0.0/product/:guid/tickets`
- **Base URL:** `https://api.weeztix.com`
- **Official documentation:** [Get Ticket Types of Product Type](https://docs.weeztix.com/api/dashboard/get-product-specific-tickets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guid` | path | `string` | yes | The guid of the Product Type. |
