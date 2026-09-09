# List Inventory Levels with Walmart

Retrieve the inventory level for every SKU at every ship node.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/inventories`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [List Inventory Levels](https://developer.walmart.com/us-marketplace/reference/getmultinodeinventoryforallskuandallshipnodes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sandboxToken` | path | `list<string>` | no | To run this request in the walmart sandbox choose 'bearer' token from the list. |
