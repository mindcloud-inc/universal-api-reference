# List Inventory with Cerbo

Retrieves inventory records from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/inventory`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Inventory](https://docs.cer.bo/#tag/Inventory/operation/listInventory)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | no | Filter by inventory type (e.g., "Drug (RX)", "General"). Uses partial matching. |
| `manufacturer` | query | `string` | no | Filter by manufacturer name. Uses partial matching. |
| `include_deleted` | query | `string` | no | Set to the string 'true' to include soft-deleted items. Other values are ignored. |
| `include_discontinued` | query | `string` | no | Set to the string 'true' to include discontinued items. Other values are ignored. |
