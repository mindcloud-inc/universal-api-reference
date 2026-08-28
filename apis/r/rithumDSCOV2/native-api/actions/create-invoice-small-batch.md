# Create Invoice Small Batch with Rithum DSCO

## Endpoint

- **Method:** `POST`
- **Path:** `invoice/batch/small`
- **Base URL:** `https://api.dsco.io/api/v3`
- **Official documentation:** [Create Invoice Small Batch](https://api.dsco.io/doc/v3/reference/#tag/Invoice/operation/createInvoiceSmallBatch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoices[]` | body | `array<object>` | yes | Array of invoice objects to create in one small batch request. |
