# List Sales Orders with DateX

## Endpoint

- **Method:** `POST`
- **Path:** `sales_orders/get`
- **Base URL:** `https://{environment}.wavelength.host/api/`
- **Official documentation:** [List Sales Orders](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_sales_orders_get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters.owner` | body | `string` | no | Owner filter. |
| `filters.project` | body | `string` | no | Project filter. |
| `filters.warehouse` | body | `string` | no | Warehouse filter. |
| `filters.status` | body | `string` | no | Status filter. |
| `filters.lookup` | body | `string` | no | Sales order lookup filter. |
| `filters.order_id` | body | `number` | no | Numeric order ID filter. |
