# List Sales Orders with DateX (Legacy)

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
| `exclude.user_defined_fields` | body | `boolean` | no | Format: `toggle`. |
| `filters` | body | `object` | no | — |
| `filters.order_id` | body | `number` | no | — |
| `exclude` | body | `object` | no | — |
| `filters.created_from` | body | `string` | no | — |
| `as_export` | body | `boolean` | no | Set this to true to get only new data that haven't been exported before |
| `filters.owner` | body | `string` | no | — |
| `filters.project` | body | `string` | no | — |
| `filters.warehouse` | body | `string` | no | — |
| `filters.status` | body | `string` | no | — |
| `filters.created_to` | body | `string` | no | — |
| `filters.fulfilled_from` | body | `string` | no | — |
| `filters.fulfilled_to` | body | `string` | no | — |
| `filters.lookup` | body | `string` | no | Use this to lookup an external order id. |
