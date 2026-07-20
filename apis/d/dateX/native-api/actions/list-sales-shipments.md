# List Sales Shipments with DateX (Legacy)

## Endpoint

- **Method:** `POST`
- **Path:** `sales_orders/shipments/get`
- **Base URL:** `https://{environment}.wavelength.host/api/`
- **Official documentation:** [List Sales Shipments](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_sales_orders_shipments_get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exclude.user_defined_fields` | body | `boolean` | no | — |
| `filters` | body | `object` | no | — |
| `filters.owner` | body | `string` | no | — |
| `paging.top` | body | `number` | no | — |
| `filters.project` | body | `string` | no | — |
| `paging` | body | `object` | no | — |
| `paging.skip` | body | `number` | no | — |
| `exclude_transmitted` | body | `boolean` | no | This will only return shipments that haven't been previously queries with this flag set to true - IF false will do a comprehensive search or don't want to flag orders as having been transmitted and exclude them from future queries |
| `filters.warehouse` | body | `string` | no | — |
| `exclude` | body | `object` | no | — |
| `filters.status` | body | `string` | no | — |
| `filters.lookup` | body | `string` | no | — |
| `filters.order_lookup` | body | `string` | no | — |
| `filters.carrier` | body | `string` | no | — |
| `filters.carrier_service_type` | body | `string` | no | — |
| `filters.created_from` | body | `date` | no | — |
| `filters.created_to` | body | `date` | no | — |
| `filters.shipped_from` | body | `date` | no | — |
| `filters.shipped_to` | body | `date` | no | — |
