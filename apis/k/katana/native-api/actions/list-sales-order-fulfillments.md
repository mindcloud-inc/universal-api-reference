# List Sales Order Fulfillments with Katana

Lists sales order fulfillments in Katana.

## Endpoint

- **Method:** `GET`
- **Path:** `/sales_order_fulfillments`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [List Sales Order Fulfillments](https://developer.katanamrp.com/reference/list-all-sales-order-fulfillments)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sales_order_id` | query | `number` | no | Filters sales order fulfillments by a sales order id |
| `picked_date_min` | query | `string` | no | Filters sales order fulfillments by a picked date min |
| `tracking_number` | query | `string` | no | Filters sales order fulfillments by a tracking number |
| `tracking_url` | query | `string` | no | Filters sales order fulfillments by a tracking url |
| `tracking_carrier` | query | `string` | no | Filters sales order fulfillments by a tracking carrier |
| `tracking_method` | query | `string` | no | Filters sales order fulfillments by a tracking method |
| `status` | query | `string` | no | Filters sales order fulfillments by a status |
| `include_deleted` | query | `boolean` | no | Soft-deleted data is excluded from result set by default. Set to true to include it. |
| `created_at_min` | query | `string` | no | Minimum value for created_at range. Must be compatible with ISO 8601 format |
| `created_at_max` | query | `string` | no | Maximum value for created_at range. Must be compatible with ISO 8601 format |
| `updated_at_min` | query | `string` | no | Minimum value for updated_at range. Must be compatible with ISO 8601 format |
| `updated_at_max` | query | `string` | no | Maximum value for updated_at range. Must be compatible with ISO 8601 format |
