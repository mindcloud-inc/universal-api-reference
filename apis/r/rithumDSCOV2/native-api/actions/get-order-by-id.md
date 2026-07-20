# Get Order with Rithum DSCO

Retrieves an order from Rithum DSCO.

## Endpoint

- **Method:** `GET`
- **Path:** `order`
- **Base URL:** `https://api.dsco.io/api/v3`
- **Official documentation:** [Get Order](https://api.dsco.io/doc/v3/reference/#tag/Order/operation/getOrderById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderKey` | query | `string` | yes | Required identifier key used to find the order. |
| `value` | query | `string` | yes | Required identifier value used to find the order. |
