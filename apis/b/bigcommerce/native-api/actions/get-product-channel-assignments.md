# Get Product Channel Assignments with BigCommerce

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/catalog/products/channel-assignments`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_id:in` | query | `string` | no | Send multiple values as a string. |
| `product_id:in` | query | `string` | no | Send multiple values as a string. |
