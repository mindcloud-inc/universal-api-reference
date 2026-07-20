# Get Inventory with Cerbo

Retrieves inventory item details from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/inventory/:id`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Get Inventory](https://docs.cer.bo/#tag/Inventory/operation/showInventory)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The inventory item ID |
| `include_deleted` | query | `boolean` | no | Set to true to retrieve soft-deleted items. |
