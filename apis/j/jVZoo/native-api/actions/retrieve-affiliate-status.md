# Retrieve Affiliate Status with JVZoo

Retrieves affiliate status for a JVZoo product.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/:product_id/affiliates/:affiliate_id`
- **Base URL:** `https://api.jvzoo.com/v2.0`
- **Official documentation:** [Retrieve Affiliate Status](https://api.jvzoo.com/docs/versions/v2.0.html#affiliate-status-affiliate-status-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `affiliate_id` | path | `number` | yes | The ID of the affiliate. |
| `product_id` | path | `number` | yes | The ID of the product. |
