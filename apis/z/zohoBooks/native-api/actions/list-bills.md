# List Bills with Zoho Books

## Endpoint

- **Method:** `GET`
- **Path:** `/bills`
- **Base URL:** `https://www.zohoapis.com/books/v3`
- **Official documentation:** [List Bills](https://www.zoho.com/books/api/v3/bills/#list-bills)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bill_number` | query | `string` | no | Filter bills by bill number. |
| `date` | query | `string` | no | Filter bills by bill date. |
| `description` | query | `string` | no | Filter bills by description. |
| `filter_by` | query | `string` | no | Filter bills by Zoho status constants. |
| `item_id` | query | `string` | no | Filter bills by item ID. |
| `last_modified_time` | query | `string` | no | Filter bills by last modification time. |
| `organization_id` | query | `string` | yes | ID of the organization. |
| `purchaseorder_id` | query | `string` | no | Filter bills by purchase order ID. |
| `recurring_bill_id` | query | `string` | no | Filter bills by recurring bill ID. |
| `reference_number` | query | `string` | no | Filter bills by reference number. |
| `search_text` | query | `string` | no | Search across bill fields. |
| `sort_column` | query | `string` | no | Sort bills by the selected column. |
| `sort_order` | query | `string` | no | Sort bills in ascending (A) or descending (D) order. |
| `status` | query | `string` | no | Filter bills by status. |
| `total` | query | `number` | no | Filter bills by total amount. |
| `vendor_id` | query | `string` | no | Filter bills by vendor ID. |
| `vendor_name` | query | `string` | no | Filter bills by vendor name. |
