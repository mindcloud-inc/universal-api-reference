# List Customer Addresses with BigCommerce

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/customers/addresses`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id:in` | query | `string` | no | Filter by the ID of the customer. Also accepts comma-separated IDs to filter for multiple customers. customer_id:in=23,24,55 Send multiple values as a string. |
| `id:in` | query | `string` | no | Send multiple values as a array. |
