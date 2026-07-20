# List Purchase Orders with Katana

Lists purchase orders in your Katana account.

## Endpoint

- **Method:** `GET`
- **Path:** `/purchase_orders`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [List Purchase Orders](https://developer.katanamrp.com/reference/findpurchaseorders)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | query | `array<number>` | no | Filters purchase orders by an array of IDs |
| `order_no` | query | `string` | no | Filters purchase orders by an order number |
| `entity_type` | query | `string` | no | Filters purchase orders by an entity type |
| `status` | query | `string` | no | Filters purchase orders by a status |
| `billing_status` | query | `string` | no | Filters purchase orders by a billing status |
| `currency` | query | `string` | no | Filters purchase orders by a currency |
| `location_id` | query | `number` | no | Filters purchase orders by a location |
| `tracking_location_id` | query | `number` | no | Filters purchase orders by a tracking location |
| `supplier_id` | query | `number` | no | Filters purchase orders by a supplier |
| `extend[]` | query | `array<string>` | no | Array of objects that need to be added to the response |
| `include_deleted` | query | `boolean` | no | Soft-deleted data is excluded from result set by default. Set to true to include it. |
| `created_at_min` | query | `string` | no | Minimum value for created_at range. Must be compatible with ISO 8601 format |
| `created_at_max` | query | `string` | no | Maximum value for created_at range. Must be compatible with ISO 8601 format |
| `updated_at_min` | query | `string` | no | Minimum value for updated_at range. Must be compatible with ISO 8601 format |
| `updated_at_max` | query | `string` | no | Maximum value for updated_at range. Must be compatible with ISO 8601 format |
