# Create Sales Order with Halo Service Solutions

Creates a new sales order in Halo Service Solutions.

## Endpoint

- **Method:** `POST`
- **Path:** `/SalesOrder`
- **Base URL:** `https://mindcloud.halopsa.com/api`
- **Official documentation:** [Create Sales Order](https://usehalo.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `[]` | body | `array<object>` | no | Sales order payload array. |
| `[].title` | body | `string` | no | Sales order title. |
| `[].client_id` | body | `number` | no | Client ID for the sales order. |
| `[].user_id` | body | `number` | no | User ID for the sales order. |
| `[].site_id` | body | `number` | no | Site ID for the sales order. |
| `[].assigned_agent` | body | `number` | no | Assigned agent ID for the sales order. |
| `[].note` | body | `string` | no | Optional note for the sales order. |
