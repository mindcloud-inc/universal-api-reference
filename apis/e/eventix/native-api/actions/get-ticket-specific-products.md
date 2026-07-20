# Retrieve all Product Types attached to this Ticket Type with Eventix

Retrieves product types for an Eventix ticket type.

## Endpoint

- **Method:** `GET`
- **Path:** `/3.0.0/ticket/:guid/products`
- **Base URL:** `https://api.weeztix.com`
- **Official documentation:** [Retrieve all Product Types attached to this Ticket Type](https://docs.weeztix.com/api/dashboard/get-ticket-specific-products)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guid` | path | `string` | yes | The guid of the Ticket Type. |
