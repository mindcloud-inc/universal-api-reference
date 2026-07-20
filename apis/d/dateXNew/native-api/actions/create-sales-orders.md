# Create Sales Orders with DateX

## Endpoint

- **Method:** `POST`
- **Path:** `sales_orders/create`
- **Base URL:** `https://{environment}.wavelength.host/api/`
- **Official documentation:** [Create Sales Orders](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_sales_orders_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orders[]` | body | `array<object>` | yes | Array of sales order objects to create, matching the documented orders schema. |
