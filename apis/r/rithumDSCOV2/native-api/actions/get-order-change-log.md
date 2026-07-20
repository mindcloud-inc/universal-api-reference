# Get Order Change Log with Rithum DSCO

Retrieves the order change log from Rithum DSCO.

## Endpoint

- **Method:** `GET`
- **Path:** `order/log`
- **Base URL:** `https://api.dsco.io/api/v3`
- **Official documentation:** [Get Order Change Log](https://api.dsco.io/doc/v3/reference/#tag/Order/operation/getOrderChangeLog)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate` | query | `date` | no | Start date for DSCO order change-log filtering. |
| `endDate` | query | `date` | no | End date for DSCO order change-log filtering. |
