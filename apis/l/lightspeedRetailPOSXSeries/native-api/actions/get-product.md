# Get Product with Lightspeed Retail POS (X-Series)

Retrieves a product from Lightspeed Retail POS (X-Series).

## Endpoint

- **Method:** `GET`
- **Path:** `/api/2.0/products/:product_id`
- **Base URL:** `https://{domain_prefix}.retail.lightspeed.app`
- **Official documentation:** [Get Product](https://x-series-api.lightspeedhq.com/reference/getproductbyid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `string` | yes | The Lightspeed product ID to retrieve. |
