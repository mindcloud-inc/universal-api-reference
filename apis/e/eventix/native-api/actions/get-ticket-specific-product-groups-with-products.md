# Get all ProductGroups with Product Types for this Ticket Type with Eventix

Retrieves product groups with products for an Eventix ticket type.

## Endpoint

- **Method:** `GET`
- **Path:** `/3.0.0/ticket/:guid/groups/products`
- **Base URL:** `https://api.weeztix.com`
- **Official documentation:** [Get all ProductGroups with Product Types for this Ticket Type](https://docs.weeztix.com/api/dashboard/get-ticket-specific-product-groups-with-products)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guid` | path | `string` | yes | The guid of the Ticket Type. |
