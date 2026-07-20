# Get Warehouses with Rithum DSCO

Lists warehouses in Rithum DSCO.

## Endpoint

- **Method:** `GET`
- **Path:** `warehouse/page`
- **Base URL:** `https://api.dsco.io/api/v3`
- **Official documentation:** [Get Warehouses](https://api.dsco.io/doc/v3/reference/#tag/Warehouse/operation/getWarehouses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scrollId` | query | `string` | no | Scroll identifier for additional warehouse result pages. |
| `status` | query | `string` | no | Filter warehouses by status. |
| `supplierId` | query | `string` | no | Filter warehouses by supplier ID. |
| `name` | query | `string` | no | Filter warehouses by name. |
