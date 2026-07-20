# Create Sales Order Lines with DateX

## Endpoint

- **Method:** `POST`
- **Path:** `sales_order_lines/create`
- **Base URL:** `https://{environment}.wavelength.host/api/`
- **Official documentation:** [Create Sales Order Lines](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_sales_order_lines_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_lines[]` | body | `array<object>` | yes | Array of sales order line objects to create, matching the documented order_lines schema. |
