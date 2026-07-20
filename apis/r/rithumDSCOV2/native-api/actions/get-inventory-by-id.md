# Get Inventory Object with Rithum DSCO

Retrieves an inventory record from Rithum DSCO.

## Endpoint

- **Method:** `GET`
- **Path:** `inventory`
- **Base URL:** `https://api.dsco.io/api/v3`
- **Official documentation:** [Get Inventory Object](https://api.dsco.io/doc/v3/reference/#tag/Inventory/operation/getInventoryById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemKey` | query | `string` | yes | Required identifier key used to find the inventory object. |
| `value` | query | `string` | yes | Required identifier value used to find the inventory object. |
