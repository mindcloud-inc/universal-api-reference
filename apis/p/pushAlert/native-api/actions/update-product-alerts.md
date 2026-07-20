# Update Product Alerts with PushAlert

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/v2/web-push/product/update`
- **Base URL:** `https://api.pushalert.co`
- **Official documentation:** [Update Product Alerts](https://pushalert.co/documentation/rest-api-v2/web-push#rest-api-price-drop-in-stock-alerts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_info` | body | `string` | yes | JSON object string describing the product and changed field. |
