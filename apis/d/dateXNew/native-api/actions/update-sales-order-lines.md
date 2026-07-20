# Update Sales Order Lines with DateX

## Endpoint

- **Method:** `POST`
- **Path:** `sales_order_lines/update`
- **Base URL:** `https://{environment}.wavelength.host/api/`
- **Official documentation:** [Update Sales Order Lines](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_sales_order_lines_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_lines[]` | body | `array<object>` | yes | Array of sales order line objects to update, matching the documented order_lines schema. |
