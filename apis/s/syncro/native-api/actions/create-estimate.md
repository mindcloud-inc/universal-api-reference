# Create Estimate with Syncro

Creates a new estimate in Syncro.

## Endpoint

- **Method:** `POST`
- **Path:** `/estimates`
- **Base URL:** `https://mindcloud.syncromsp.com/api/v1`
- **Official documentation:** [Create Estimate](https://api-docs.syncromsp.com/#/Estimate/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | body | `number` | yes | Required customer record ID for the estimate. |
| `date` | body | `date` | yes | Required estimate date. |
| `number` | body | `string` | no | — |
| `name` | body | `string` | no | — |
| `status` | body | `string` | no | Valid values are Fresh, Draft, Approved, Declined. |
| `ticket_id` | body | `number` | no | — |
| `location_id` | body | `number` | no | — |
| `note` | body | `string` | no | — |
| `line_items[]` | body | `array<object>` | no | Array of estimate line item objects. |
| `line_items[].item` | body | `string` | no | — |
| `line_items[].name` | body | `string` | no | — |
| `line_items[].product_id` | body | `number` | no | — |
| `line_items[].quantity` | body | `number` | no | — |
| `created_at` | body | `date` | no | — |
| `updated_at` | body | `date` | no | — |
