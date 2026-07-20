# Update Sales Orders with DateX

## Endpoint

- **Method:** `POST`
- **Path:** `sales_orders/update`
- **Base URL:** `https://{environment}.wavelength.host/api/`
- **Official documentation:** [Update Sales Orders](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_sales_orders_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sales_orders[]` | body | `array<object>` | yes | Array of sales order objects to update, matching the documented sales_orders schema. |
