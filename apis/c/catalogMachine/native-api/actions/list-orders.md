# List Orders with Catalog Machine

Retrieves all orders from Catalog Machine.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders`
- **Base URL:** `https://www.catalogmachine.com/api/v1`
- **Official documentation:** [List Orders](https://help.catalogmachine.com/en/articles/3667421-rest-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Optional order status filter (for example Approved). |
