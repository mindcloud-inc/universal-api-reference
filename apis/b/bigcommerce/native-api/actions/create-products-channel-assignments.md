# Create Products Channel Assignments with BigCommerce

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/catalog/products/channel-assignments`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `product_id` | body | `number` | yes |
| `channel_id` | body | `number` | yes |
