# Get Invoice with Rithum DSCO

Retrieves an invoice from Rithum DSCO.

## Endpoint

- **Method:** `GET`
- **Path:** `invoice`
- **Base URL:** `https://api.dsco.io/api/v3`
- **Official documentation:** [Get Invoice](https://api.dsco.io/doc/v3/reference/#tag/Invoice/operation/getInvoiceById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | query | `string` | yes | Required identifier key used to find the invoice. |
| `value` | query | `string` | yes | Required identifier value used to find the invoice. |
