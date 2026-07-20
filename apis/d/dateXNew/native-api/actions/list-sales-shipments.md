# List Sales Shipments with DateX

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
| `filters.order_lookup` | body | `string` | no | Sales order lookup filter. |
| `filters.lookup` | body | `string` | no | Shipment lookup filter. |
| `filters.carrier` | body | `string` | no | Carrier filter. |
| `exclude_transmitted` | body | `boolean` | no | Exclude transmitted shipments. |
