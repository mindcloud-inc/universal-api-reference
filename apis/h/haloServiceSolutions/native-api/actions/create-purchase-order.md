# Create Purchase Order with Halo Service Solutions

Creates a new purchase order in Halo Service Solutions.

## Endpoint

- **Method:** `POST`
- **Path:** `/PurchaseOrder`
- **Base URL:** `https://mindcloud.halopsa.com/api`
- **Official documentation:** [Create Purchase Order](https://usehalo.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `[]` | body | `array<object>` | no | Purchase order payload array. |
| `[].title` | body | `string` | no | Purchase order title. |
| `[].supplier_id` | body | `number` | no | Supplier ID for the purchase order. |
| `[].client_id` | body | `number` | no | Client ID for the purchase order. |
| `[].user_id` | body | `number` | no | User ID for the purchase order. |
| `[].site_id` | body | `number` | no | Site ID for the purchase order. |
| `[].assigned_agent` | body | `number` | no | Assigned agent ID for the purchase order. |
| `[].note` | body | `string` | no | Optional note for the purchase order. |
| `[].salesorder_id` | body | `number` | no | Related sales order ID. |
